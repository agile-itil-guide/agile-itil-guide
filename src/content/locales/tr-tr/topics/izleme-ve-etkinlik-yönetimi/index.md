# İzleme ve Etkinlik Yönetimi

**İzleme, bir hizmetin kullanıcıların deneyimlediği biçimde çalışıp çalışmadığını söyler; iyi etkinlik yönetimi ise bir sinyal selini, bir kişinin anlayıp harekete geçebileceği az sayıda uyarıya dönüştürür.**

## Bu neden önemli

Göremediğiniz bir hizmeti işletemezsiniz. İzleme olmadan bir ekip arızaları kullanıcılardan, yavaş çürümeyi ise hiç kimseden öğrenir. Zayıf izlemede sorun tersidir: o kadar çok uyarı vardır ki nöbetçi mühendis onlara inanmayı bırakır ve önemli olan gürültüde kaybolur. Her iki uç da uykuya, güvene ve zamana mal olur.

İzleme ve etkinlik yönetimi, bir olayın ne kadar hızlı bulunup düzeltilebileceğini de belirler. Olay yönetimindeki her şey, bir şeylerin ters gittiğini çabuk bilmeye ve nedenini bulmaya yetecek bilgiye sahip olmaya bağlıdır (bkz. Konu 3.2 — Olay Yönetimi). Sık sürüm çıkaran çevik ekiplerin buna daha da çok ihtiyacı vardır, çünkü her sürüm bir şeyi bozma fırsatıdır ve her geri alma kararı etkiyi görmeye bağlıdır.

Google'ın *Site Reliability Engineering* kitabının konuyu doğrudan ele alan iki bölümü vardır: "Monitoring Distributed Systems" ve "Practical Alerting from Time-Series Data". Bunlar bir kuruluşun uygulamasını betimler ve kasıtlı olarak basit, kullanıcıya odaklı bir yaklaşımı savunur. Bu konu, bu rehber için başvurulan Wikipedia maddeleri uygulama hakkında az şey verdiği için, bunları ana kaynak olarak kullanır. Buradaki etkinlik, uyarı ve etkinlik yönetimi gibi ITIL sözcük dağarcığı, bu rehberin çerçeve sahibinin metnine karşı doğrulayamadığı, yaygın olarak yayımlanmış betimlemelerden alınmıştır. SRE bölümlerini iyi açıklanmış bir seçenek olarak okuyun.

## Temel kavramlar

### İzleme

SRE bölümü **izlemeyi (monitoring)** bir sistem hakkındaki gerçek zamanlı nicel verilerin toplanması, işlenmesi ve görüntülenmesi olarak tanımlar. İzlemenin uzun vadeli eğilim çözümlemesini, deneyler arası karşılaştırmayı, uyarı vermeyi, panoları ve sonradan ad hoc hata ayıklamayı desteklediğini söyler. İzlemenin önemli bir mühendislik çabası olduğunu ve ekiplerin tipik olarak buna en az bir kişi atadığını vurgular.

### Etkinlikler, uyarılar ve olaylar

ITSM kullanımında **etkinlik (event)**, bir hizmetin yönetimi için önem taşıyan bir durum değişikliğidir. Çoğu etkinlik bilgilendiricidir. Bazıları bir uyarıyı ya da bir istisnayı gösterir. **Uyarı (alert)**, SRE bölümünün ifadesiyle, bir bilet, e-posta ya da çağrı (page) olarak iletilen, bir insana yönelik bildirimdir. **Olay (incident)** plansız bir kesinti ya da kalite düşüşüdür (bkz. Konu 3.2 — Olay Yönetimi). Etkinlik yönetimi, hangi etkinliklerin önemli olduğuna, onlar hakkında ne yapılacağına ve kime haber verileceğine karar verme uygulamasıdır. Akış, etkinliklerden uyarılara ve bazen olaylara doğrudur.

### Kara kutu ve beyaz kutu izleme

Bölüm iki türü ayırır:

| Tür | Ne yapar | Güçlü yanı |
|---|---|---|
| **Kara kutu (black-box)** | Dışarıdan görünen davranışı, bir kullanıcının göreceği gibi sınar | Etkin sorunları algılar; çağrı için uygundur |
| **Beyaz kutu (white-box)** | Sistemin iç yapısının sunduğu, günlükler ya da iç işleyiciler gibi ölçüleri kullanır | Yaklaşan sorunları ve yeniden denemelerle maskelenen arızaları ortaya çıkarır; hata ayıklama için vazgeçilmezdir |

Kitap ikisini birleştirir. Bir kara kutu yoklaması size ödemenin başarısız olduğunu söyler; beyaz kutu verisi nedenini bulmanıza yardımcı olur.

### Belirtiler ve nedenler

Bölüm, izlemenin iki soruyu yanıtlaması gerektiğini söyler: neyin bozuk olduğu ve nedeni. Uyarıları, kullanıcıların deneyimlediği şey olan belirtilere odaklamayı ve nedenler için ancak kesin ve yakın olduklarında çağrı göndermeyi önerir. Tek bir makinenin arızalanması, uyarı bölümündeki ifadesiyle, çok gürültülü olduğu için hakkında uyarılmanın kabul edilemez olduğu bir durumdur. Bu, iyi bir uyarı yaklaşımının özüdür: bir parça seğirdiğinde değil, kullanıcılar zarar gördüğünde ya da göreceği zaman bir insana haber verin.

### Dört altın sinyal

Bölüm, kullanıcıya dönük bir sistem için izlenecek dört sinyal önerir:

- **Gecikme (latency):** bir isteği sunma süresi. Başarısız istekleri ayrı izleyin, çünkü "yavaş bir hata, hızlı bir hatadan bile kötüdür."
- **Trafik (traffic):** sistem üzerindeki talep.
- **Hatalar (errors):** açık, örtük ya da politika gereği başarısız istekler.
- **Doygunluk (saturation):** hizmetin ne kadar "dolu" olduğu. Performans çoğunlukla %100 kullanıma ulaşmadan bozulur.

Bunlar doğal olarak hizmet seviyesi göstergelerine karşılık gelir (bkz. Konu 3.7 — Hizmet Seviyesi Yönetimi). Bölüm ayrıca ortalamaların yavaş aykırı değerleri gizlediği konusunda uyarır ve dağılımı görmek için istek sayılarını gecikme kovalarında kaydetmeyi önerir.

### İyi bir uyarıyı ne oluşturur

Bölüm, bir uyarı yazmadan önce sorulacak soruları sunar: acil, eyleme dönüştürülebilir, kullanıcı tarafından görülebilir bir durumu mu algılıyor; güvenle yok sayılabilir mi; ve yanıt otomatikleştirilebilir mi? Çağrılar eyleme dönüştürülebilir olmalı, yargı gerektirmeli ve yeni sorunlara ilişkin olmalıdır. Uyarıların asla yalnızca "bir şey biraz tuhaf görünüyor" diye tetiklenmemesi gerektiğini söyler. Yanıtları ezbere ve algoritmik olan çağrılar, ona göre, otomasyon ya da kök neden onarımı gerektiren bir kırmızı bayraktır.

### Uyarıları yönlendirme

Uyarı bölümü, çağrıya değer uyarıların nöbetçi personele, kritik olmayanların bilet kuyruklarına ve geri kalanların durum panolarına gönderilmesini betimler. Uyarıları yönlendirmek, yinelenenleri ayıklamak ve bastırmak için araçları betimler ve uyarıların dalgalanabileceği için tetiklenmeden önce asgari bir süre beklemesi gerektiğini not eder. "Yalnızca beklediğiniz arızalar için uyarı verebilirsiniz" konusunda uyarır; bu nedenle kara kutu yoklamalarını beyaz kutu verileriyle birleştirmek önemlidir.

### Basit tutun

Bölüm, eşikleri öğrenen ya da nedenselliği algılayan "sihir" yerine basit, hızlı sistemleri savunur ve karmaşık bağımlılık hiyerarşilerinin sınırlı başarı sağladığını not eder. Gerçek olayları yakalayan kuralları basit tutmayı, nadiren işletilen uyarıları ve kullanılmayan sinyalleri kaldırmayı ve bakım maliyetlerinin hizmetin boyutundan daha yavaş büyümesini sağlamayı söyler. Betimlediği örnekler, örneğin uyarıların altında ezilen ve kalıcı düzeltmelere zaman açmak için hedefini geçici olarak gevşeten ve e-posta uyarılarını devre dışı bırakan bir ekip, gürültüyü kaldırma istekliliğini gösterir.

### Panolar ve uzun vadeli görünümler

Bölüm panoları bir hizmetin ana ölçülerinin önceden hazırlanmış özet görünümleri olarak ele alır ve panoların, çok sınırlı değeri olduğunu söylediği e-posta uyarılarından daha iyi olduğunu belirtir. Ayrıca yönetimi çağrı yükünden haberdar tutmak için çağrı sıklığını, örneğin üç aylık raporlarda, zaman içinde gözden geçirmeyi önerir. Bu, uyarı kalitesini yöneticilerin görebileceği bir şeye dönüştürür (sürdürülebilir tempo için bkz. Konu 1.2 — Çevik İlkeler).

### Kaynakların sınırları

SRE bölümleri tek bir işlenmiş örneğin ötesinde eşik vermez, çalışma kılavuzlarını ya da nöbet yükü sınırlarını tartışmaz ve uyarıların zaman içinde nasıl gözden geçirilip emekliye ayrılacağını betimlemez; bunlar kendi uygulamanızın konularıdır. Güçlü mühendislik kaynaklarına sahip tek bir büyük kuruluştan gelirler. Daha küçük ekipler ilkeleri daha basit araçlarla uygulayabilir.

## İyi uygulamalar

1. **Kullanıcıların deneyimlediğini izleyin.** Oturum açma ya da sipariş verme gibi gerçek bir kullanıcı eylemini gerçekleştiren en az bir kara kutu yoklaması ekleyin ve başarısız olduğunda uyarı verin.
2. **Dört altın sinyali izleyin.** Her hizmet için gecikmeyi, trafiği, hataları ve doygunluğu izleyin. Diğer ölçüleri yalnızca sorduğunuz bir soruyu yanıtlıyorlarsa ekleyin.
3. **Belirtiler için uyarı verin.** Kullanıcılar zarar gördüğünde ya da yakında göreceğinde çağrı gönderin. Tek bir arızalı makine gibi iç durumları, kesin ve yakın olmadıkça daha düşük öncelikli bilgi olarak ele alın.
4. **Her çağrıyı eyleme dönüştürülebilir kılın.** Bir uyarı oluşturmadan önce, müdahale edenin ne yapması gerektiğini yazın. Yapılacak bir şey yoksa bu bir çağrı değildir.
5. **Aciliyete göre yönlendirin.** Acil uyarıları nöbetçiye, daha az acil olanları bir bilet kuyruğuna ve bilgiyi bir panoya gönderin. Yok sayacak kişilere e-posta uyarısı göndermeyin.
6. **Yalnızca ortalamaları değil, dağılımları kullanın.** Yavaş aykırı değerlerin görünür olması için gecikmede yüksek yüzdeliklere ya da kovalara bakın.
7. **Asgari bir süre belirleyin.** Dalgalanmayı önlemek için bir koşulun uyarı vermeden önce kısa bir süre devam etmesini isteyin. Süreyi gerçek verilerle ayarlayın.
8. **Gürültülü uyarıları emekliye ayırın.** En çok hangi uyarıların tetiklendiğini ve hiçbir eyleme yol açmadığını gözden geçirin. Kaldırın ya da düzeltin. SRE bölümü ezbere yanıtları otomasyon ya da onarım için bir sinyal olarak ele alır.
9. **İzlemenizi sınayın.** Bir sınama ortamında kasıtlı olarak bir şeyi bozun ve doğru uyarının tetiklendiğini denetleyin. İzleme sisteminin kendisini de denetimlere dahil edin, böylece arızası fark edilir.
10. **Çağrı yükünü gözden geçirin.** Her çeyrekte vardiya başına çağrıları, mesai dışı kesintileri ve yanlış alarmları sayın. Sonuçları yöneticilerle paylaşın ve planlamada kullanın.
11. **İzlemeyi bitti tanımında tutun.** Her yeni özellik için, çalışıp çalışmadığını hangi sinyallerin gösterdiğini ve varsa hangi uyarıya ihtiyaç duyduğunu sorun (bkz. Konu 3.5 — Sürüm ve Dağıtım Yönetimi).
12. **Basit tutun.** Karmaşık bir düzen yerine anlaşılır birkaç kuralı tercih edin. Kullanılmayan sinyalleri kaldırın ve kuralları olaylardan sonra gözden geçirin.

## Ekibinizle tartışılacak sorular

**Son üç olayımızdan nasıl haberdar olduk?**

Her olayı ve ilk nasıl fark edildiğini listeleyin: bir uyarı, bir kullanıcı, bir meslektaş. Çoğu kullanıcılardan geldiyse, izleme önemli olan belirtileri kaçırıyordur. Kolaylaştırıcı bir yoklamanın ne gösterebileceğini sorabilir. İlk izlenecek bir kullanıcı eylemi seçin.

**Hangi uyarıları yok sayıyoruz ve neden?**

Nöbetçi mühendislerden sessize aldıkları ya da atladıkları uyarıları isteyin. Her biri düzeltilecek ya da silinecek bir adaydır. İnsanların bir uyarıya güvenmesini ya da güvenmemesini neyin belirlediğini sorun. Açık bir yanıt çoğu zaman kimsenin harekete geçemeyeceği koşullarda tetiklenen uyarıları ortaya çıkarır. Üçünü emekliye ayırmak ya da düzeltmek üzere anlaşın.

**Nöbette yaşadığımız en kötü gece hangisiydi ve onu ne daha iyi yapardı?**

Suçlamadan hikâyeler toplayın. Örüntülere bakın: yinelenen çağrılar, belirsiz uyarılar, çalışma kılavuzu eksikliği, yükseltme yokluğu. Her örüntü bir iyileştirmedir. En çok hangi iki değişikliğin yardımcı olacağını sorun. Amaç daha hafif bir yük ve daha net bir sinyaldir.

**İzleme sistemimiz arızalansa bunu nasıl anlardık?**

Gözcüyü kimin izlediğini sorun. Birçok ekibin izlemenin çalıştığına dair bir denetimi yoktur. Basit bir kalp atışı (heartbeat) ya da ayrı bir sistemden yoklamayı tartışın. Eklenecek bir denetim üzerinde anlaşın.

**Panolarımız ne gösteriyor ve onlara kim bakıyor?**

Panoları listeleyin ve her birini son ayda kimin kullandığını sorun. Kullanılmayan panolar dağınıklıktır; yararlı olanlar hizmet hakkında bir hikâye anlatır. Her birinin hangi soruyu yanıtladığını sorun. Gerçek soruları yanıtlayan küçük bir küme tutun.

**Bir sürümün işleri kötüleştirdiğini nasıl anlardık?**

Yakın tarihli bir sürüm seçin ve hangi sinyalin bir sorunu göstereceğini sorun. Yanıt "kullanıcılardan duyardık" ise, bir sürümden sonra hangi sinyallerin izleneceğini ve kimin sorumlu olduğunu tartışın. Bu soru izlemeyi dağıtıma bağlar. Kısa bir sürüm sonrası kontrol listesi yazın.

## Uygulamada: çevik bir ITIL örneği

Bir şehrin toplu taşıma idaresi, günde 400.000 kişinin kullandığı bir yolculuk planlama web sitesi ve uygulaması işletiyor. On kişilik bir platform ekibi, dört kişilik bir nöbet çizelgesiyle hizmetin sahibi. Ekibin yüzlerce uyarısı var: her sunucuda CPU, disk alanı, kuyruk uzunlukları ve hata sayıları. Nöbetçi mühendisler tipik bir haftada 40 çağrı alıyor, çoğu mesai dışında ve geçen çeyrekteki iki olay ilk olarak kullanıcılar tarafından sosyal medyada bildirildi.

Ekip lideri ve bir mühendis üç aylık çağrıları gözden geçiriyor. Dörtte üçünün eylem gerektirmeyen ya da kendiliğinden çözülen durumlar için olduğunu görüyorlar. SRE kitabından basit bir yaklaşımı izlemeyi kabul ediyorlar: kullanıcıların deneyimlediği şey için uyarı verin. Her dakika standart bir yolculuk planlayan ve başarıyı ve hızı ölçen bir yoklama ekliyorlar ve veritabanının ile kuyruğun doygunluğuna ilişkin küçük bir uyarı kümesini tutuyorlar. Geri kalanını bir panoya ve günlük bir bilete taşıyorlar. Kalan her çağrı, neyin denetleneceğini söyleyen kısa bir çalışma kılavuzu girdisi alıyor.

Bir ay sonra çağrılar haftada yaklaşık beşe düşüyor ve ardından gelen iki olay da kullanıcılar şikâyet etmeden önce yoklama tarafından algılanıyor. Bazı sorunlar sürüyor. Yoklama yalnızca bir yolculuk türünü kapsıyor ve bisikletle yolculukları etkileyen bir arıza bir gün boyunca fark edilmedi. Bir mühendis ayrıca "panoya taşıma" kararının daha sonra bir arızaya yol açan yavaş bir disk sorununu gizlediğini bildiriyor. Ekip diğer yolculuk türleri için yoklamalar ekliyor, nöbet çizelgesine panonun günlük gözden geçirmesini ekliyor ve çağrı yükünü her çeyrekte gözden geçirmeyi kabul ediyor.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri yazılımın ne yapması gerektiğini ve nerede başarısız olabileceğini bilir. Sinyalleri koda yerleştirin: yararlı günlükler, ölçüler ve sağlık denetimleri. Kilit kullanıcı eylemleri için yoklamalar tanımlayın ve izlemeyi bitti tanımının parçası olarak ele alın. Çağrıların gerçek sorunları yansıtması için uyarı gözden geçirmelerine katılın.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri çağrı cihazını ve panoları taşır. Uyarıları az ve eyleme dönüştürülebilir tutun, aciliyete göre yönlendirin ve çağrı yükünü izleyin. Gürültülü uyarıları kanıtla birlikte sahibi olan ekiplere geri gönderin ve olaylardan neyin izlenmesi gerektiği hakkında öğrendiklerinizi paylaşın.

### Liderlik ve yönetişim

Liderler daha fazla uyarı değil, çağrı yükü ve olay algılama verilerini istemelidir. Gürültüyü emekliye ayırmak ve yararlı sinyaller eklemek için zamanı destekleyin. Mesai dışı çağrıların artan sayısını hizmet ve insanlar için bir risk olarak ele alın.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar, sorunlar onlar fark etmeden bulunduğunda yarar sağlar. Sorunları neyi ne zaman denediğiniz gibi ayrıntılarla bildirin, çünkü bu izlemeyi ayarlamaya yardımcı olur. Sağlayıcılara arızaları nasıl ve ne kadar hızlı algıladıklarını ve durum bilgisi yayımlayıp yayımlamadıklarını sorun.

## Yaygın başarısızlık biçimleri

- **Her şey için uyarı vermek.** Çağrı cihazı sürekli öter ve güven kaybolur. Bunun yerine belirtiler için çağrı gönderin ve gerisini biletlere ya da panolara yönlendirin.
- **Kullanıcıları değil sistemleri izlemek.** Kullanıcılar oturum açamazken tüm makineler yeşildir. Bunun yerine gerçek kullanıcı eylemlerinin kara kutu yoklamalarını ekleyin.
- **Eylem eklenmemiş.** Çağrılar yapılacak bir şey olmadan gelir. Bunun yerine her çağrının betimlenmiş bir yanıtı olmasını isteyin ya da kaldırın.
- **Yalnızca ortalamalar.** Ortalama iyi görünürken bir kullanıcı grubu acı çeker. Bunun yerine yüksek yüzdeliklere ya da dağılımlara bakın.
- **Karmaşık, akıllı kurallar.** Öğrenilmiş eşikler ve bağımlılık ağaçları müdahale edenleri şaşırtır. Bunun yerine basit, anlaşılır kuralları tercih edin.
- **İzlenmeyen izleme.** İzleme sistemi sessizce arızalanır. Bunun yerine kalp atışları ve sınamalarla denetleyin.
- **Ezbere yanıtlar.** İnsanlar her çağrıdan sonra aynı düzeltmeyi yinelir. Bunun yerine yanıtı otomatikleştirin ya da nedeni düzeltin.
- **Çağrı yükünü göz ardı etmek.** Gece çağrıları normal sayılır. Bunun yerine bunları ölçün ve gözden geçirin ve yüksek yükü bir risk olarak ele alın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Kullanıcı deneyiminin görünürlüğü | Sorunların çoğunu kullanıcılar bildirir | Bazı hizmetlerin kullanıcı eylemleri için yoklamaları ya da ölçüleri vardır | Kilit kullanıcı eylemleri yoklanır ve her hizmet için altın sinyaller izlenir | Algılama süresi ve kapsam ölçülür ve boşluklar giderilir | İzleme ekipler, tedarikçiler ve müşteriler arasında paylaşılır |
| Uyarı kalitesi | Çok uyarı, az eylem | Bazı ekipler uyarıları budar | Çağrılar belirti tabanlı, eyleme dönüştürülebilir ve aciliyete göre yönlendirilmiştir | Uyarı kesinliği ve gürültü ölçülür ve gözden geçirilir | Uyarı tasarımı ortak kanıtlardan ekipler arasında iyileştirilir |
| Yanıt ve otomasyon | Yanıtlar doğaçlamadır | Bazı çalışma kılavuzları vardır | Çağrılar çalışma kılavuzlarına bağlanır ve ezbere yanıtlar otomatikleştirilir | Yanıt süresi ve otomasyon kullanımı ölçülür | Yanıtlar ekipler ve tedarikçiler arasında eşgüdümlüdür |
| İnsanlar ve yük | Çağrı yükü izlenmez | Bazı ekipler çağrıları sayar | Çağrı yükü her çeyrekte gözden geçirilir | Yük verilerden dengelenir ve azaltılır | Yük ve öğrenme ekipler arasında paylaşılır ve planlamaya yansıtılır |

## Kontrol listesi

- [ ] Her önemli hizmetin gerçek bir kullanıcı eyleminin en az bir yoklaması var.
- [ ] Her hizmet için gecikmeyi, trafiği, hataları ve doygunluğu izliyoruz.
- [ ] Her çağrının yazılı bir yanıtı var ve kullanıcının görebileceği ya da yakın bir durumla ilgili.
- [ ] Uyarılar aciliyete göre nöbetçiye, biletlere ya da panolara yönlendirilir.
- [ ] Gecikme için yüksek yüzdelikler ya da dağılımlar görünürdür.
- [ ] En çok hangi uyarıların tetiklendiğini gözden geçiriyor ve eyleme yol açmayanları emekliye ayırıyoruz.
- [ ] İzleme sisteminin kendisi denetlenir.
- [ ] Çağrı yükü (vardiya başına çağrılar, mesai dışı kesintiler) her çeyrekte gözden geçirilir.
- [ ] Yeni özellikler bitti tanımlarında izlemeyi içerir.
- [ ] Her sürümden sonra biri sinyalleri kısa bir listeye karşı denetler.

## Yapay zeka istemleri

**Amaç: bir uyarı listesini gürültü ve eyleme dönüştürülebilirlik açısından gözden geçirmek.**

```text
Here is a list of our alerts with how often each fired in the last [period], and what happened after (acted on, ignored, resolved by itself): [paste as a table; use real data].

Using only my data, group the alerts into: fired often with no action; fired and led to action; rarely fired. For each of the first group, suggest a question to ask its owner (for example whether it can be removed, routed to a ticket, or turned into a symptom-based alert). Do not invent frequencies or outcomes. Tell me what additional data would help, and list what you are unsure of.
```

**Amaç: bir kullanıcı yolculuğu için bir yoklama tanımlamak.**

```text
Help me define a black-box probe for this user action in [service]: [describe, for example "a user searches for a journey and receives results"].

What counts as success: [describe].
What is too slow: [say "unknown" or describe in words, not numbers].
What systems the action touches: [list].

Describe the steps the probe should perform, what it should record (success, time taken, and where it failed), what alert condition to propose (leave thresholds as [to be agreed]), and what a responder would check first. Mark assumptions. Do not invent system details. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bir uyarı için yanıt bölümünü yazmak.**

```text
For this alert, write a short response entry for on-call staff.

Alert name and condition: [paste].
What it means for users: [describe].
What I know to check first: [list].
Who to escalate to: [role, or write "unknown"].

Write: what the alert means, the first three checks, how to tell whether users are affected, when to escalate, and a note on whether the response could be automated. Use only my information; mark anything you added as [CHECK]. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: üç aylık bir çağrı yükü gözden geçirmesi hazırlamak.**

```text
Help me prepare a quarterly pager load review for [team].

Data for the quarter (pages by week, out-of-hours pages, pages with no action, incidents detected by monitoring versus by users): [paste real figures].
Context: [describe changes in the period].

Summarize the data in plain language, using only my figures. Highlight trends and outliers as questions, not conclusions. Suggest three questions for the team and one for management. Do not invent causes. If the data is incomplete, say what to collect. List what you are unsure of.
```

## Yapay zeka becerileri

- [runbook](../../../../skills/runbook/SKILL.md): her çağrıyla birlikte giden yanıtı yazmak için kullanın.
- [on-call-rotation](../../../../skills/on-call-rotation/SKILL.md): adil bir nöbet çizelgesi tasarlamak ve çağrı yükünün nasıl paylaşılıp gözden geçirileceğini planlamak için kullanın.
- [software-engineering-metrics](../../../../skills/software-engineering-metrics/SKILL.md): hizmet ve teslimat performansı ölçülerini seçmek ve yorumlamak için kullanın.
- [performance-testing](../../../../skills/performance-testing/SKILL.md): sorunlar kullanıcılara ulaşmadan önce yük altında gecikmeyi ve doygunluğu denetlemek için kullanın.
- [chaos-testing](../../../../skills/chaos-testing/SKILL.md): güvenli bir ortamda arızaları kasıtlı olarak oluşturarak bunların algılanıp ele alındığını sınamak için kullanın.

## Temel kaynaklar

- **Monitoring Distributed Systems** (*Site Reliability Engineering*, Google, sre.google): tanımlar, dört altın sinyal, belirtiler ve nedenler ve basit uyarı üzerine tavsiyeler.
- **Practical Alerting from Time-Series Data** (*Site Reliability Engineering*, Google, sre.google): uyarı kurallarının, yönlendirmenin ve dalgalanmanın pratikte nasıl işlediği.
- **Service Level Objectives** (*Site Reliability Engineering*, Google, sre.google): göstergeler, hedefler ve uyarılar arasındaki bağlantı.
- **IT service management** (Wikipedia): izlemenin ve olayların ITSM'deki yeri.

## Kaynakça

1. Monitoring Distributed Systems — Google SRE book, sre.google — https://sre.google/sre-book/monitoring-distributed-systems/
2. Practical Alerting from Time-Series Data — Google SRE book, sre.google — https://sre.google/sre-book/practical-alerting/
3. Service Level Objectives — Google SRE book, sre.google — https://sre.google/sre-book/service-level-objectives/
4. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
5. Network monitoring — Wikipedia — https://en.wikipedia.org/wiki/Network_monitoring
6. Observability (software) — Wikipedia — https://en.wikipedia.org/wiki/Observability_(software)
7. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
8. Alarm fatigue — Wikipedia — https://en.wikipedia.org/wiki/Alarm_fatigue
9. Incident management — Wikipedia — https://en.wikipedia.org/wiki/Incident_management
