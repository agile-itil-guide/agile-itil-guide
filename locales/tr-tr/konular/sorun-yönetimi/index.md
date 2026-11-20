# Sorun Yönetimi

**Sorun yönetimi, tekrarlayan olayların ardındaki nedenleri bulup ortadan kaldırır; çevik biçimi, ara sıra yapılan büyük soruşturmalar yerine iş listesinde kanıta dayalı küçük düzeltmelerin sürekli akışıdır.**

## Bu neden önemli

Olayları iyi ele alan ama nedenlerini asla ortadan kaldırmayan bir ekip koşu bandındadır. Her kesinti onarılır, aynı arıza geri döner ve nöbetçi mühendisler yorulur. Sorun yönetimi koşu bandından inen uygulamadır: olayın neden olduğunu, yeniden olup olmayacağını ve neyin onu durduracağını sorar.

Çevik ekipler bunu yapmak için iyi konumdadır. Bir düzeltmenin bir özellikle rekabet edebildiği bir iş listeleri, küçük düzeltmeleri ucuz kılan kısa döngülerle çalışırlar ve örüntülerin fark edilebileceği retrospektifler yaparlar. Çoğu zaman eksik olan, olayları birbirine bağlama alışkanlığı ve nedenleri düzgün aramanın disiplinidir. Sorun yönetimi ikisini de sağlar.

[Kök neden analizi hakkındaki Wikipedia maddesi](https://en.wikipedia.org/wiki/Root_cause_analysis), bu konu için okunan ana kaynaktır; çünkü İngilizce Wikipedia'da kontrol edilen adreste "Problem management" başlıklı bir madde yoktur. Bu madde, kök neden analizini (RCA) BT operasyonlarında ve diğer alanlarda kullanılan bir problem çözme yöntemi olarak anlatır ve eksik atıflar için bakım etiketleri taşır. Burada kullanılan bilinen hata ve geçici çözüm gibi ITIL sözcük dağarcığı, uygulamanın yaygın biçimde yayımlanmış anlatımlarından gelir; bu kılavuz bunları çerçeve sahibinin metnine karşı doğrulayamadı. Kesin tanımlar önemli olduğunda sahibinin güncel yayınlarını okuyun (bkz. Konu 2.2 — ITIL).

## Temel kavramlar

### Olay, sorun, bilinen hata

Üç terim birlikte kullanılır ve ayrımlar önemlidir:

| Terim | ITSM'de yaygın kullanımıyla anlamı | Örnek |
|---|---|---|
| **Olay** (incident) | Bir hizmette planlanmamış bir kesinti veya kalitesinde azalma | Rezervasyon sayfası yirmi dakika çalışmıyor |
| **Sorun** (problem) | Bir veya daha fazla olayın altta yatan veya olası nedeni | Rezervasyon hizmetinde bir bellek sızıntısı |
| **Bilinen hata** (known error) | Nedeni belirlenmiş, genellikle bir geçici çözümün kaydedildiği sorun | Bir bellek sızıntısı anlaşılmıştır; düzeltilene kadar hizmetin her gece yeniden başlatılması kesintileri önler |

**Geçici çözüm** (workaround), bir olayın veya sorunun etkisini nedenini ortadan kaldırmadan azaltmanın ya da önlemenin bir yoludur. Sorun yönetimi nedeni ortadan kaldırmakla ilgilidir; olay yönetimi ise hizmeti geri getirmekle ilgilidir (bkz. Konu 3.2 — Olay Yönetimi).

### Tepkisel ve proaktif

Kök neden analizi maddesi tepkisel ve proaktif yaklaşımları genel terimlerle ayırır. Tepkisel iş belirtileri hızla ele alır. Proaktif iş sorunları önlemeyi amaçlar ve tanı doğruluğunu hızın önüne koyar. ITSM uygulamasında ikisi de vardır: tepkisel sorun yönetimi olaylardan sonra sorunları araştırır ve proaktif sorun yönetimi, olaylara yol açmadan önce örüntüleri ve zayıflıkları arar.

### Kök neden nedir

Madde, kök nedeni pratik bir sınamayla tanımlar: bir etken, ortadan kaldırılması sorunun yinelenmesini önlüyorsa sorunun kök nedenidir. Kök nedeni diğer nedensel etkenlerden ayırır. Bu yararlı bir kuraldır. Bir etkeni ortadan kaldırırsanız ve sorun yine de geri dönebiliyorsa, bir katkıda bulunan bulmuşsunuzdur; kök değil.

Madde ayrıca sınırlar konusunda uyarır. Eksik izleme verilerinin, çok yüksek etkinlik hacimlerinin, birden çok kök nedenin ve yüzeysel bir kökte duran araştırmacıların çözümlemeyi karmaşıklaştırdığını söyler. BT'de RCA'nın çoğu zaman hata ağaçlarından veya tasarım şartnamelerinden yoksun olduğunu, bu nedenle "kök neden yoktur"un yaygın bir söz hâline geldiğini not eder. Karmaşık sistemler için tek bir suçlu değil, birkaç katkıda bulunan neden bekleyin.

### Kök neden analizinin ilkeleri

Madde genel adımları listeler:

1. Sorunu net biçimde tanımlayın.
2. Normal işletimden arızaya bir zaman çizelgesi oluşturun.
3. Kök nedeni diğer nedensel etkenlerden ayırın.
4. Kök nedeni soruna bağlayan bir nedensellik grafiği çizin.

Araştırmacıların başarısız olan veya eksik olan savunmalara (bariyer analizi) bakması, soruşturma çizgilerinde yanlılıktan kaçınması, düzeltici eylemlere karar vermesi ve bu eylemlerin etkili olup olmadığını gözden geçirmesi gerektiğini ekler.

### Yöntemler

Madde, ISO/IEC 31010'a göre RCA'nın beş neden, hata modu ve etkileri analizi (FMEA), hata ağacı analizi, Ishikawa (balık kılçığı) diyagramları ve Pareto analizi kullanabileceğini söyler. Adını taşıyan nedensellik diyagramını Kaoru Ishikawa'ya atfeder. Ayrıca balık kılçığı ve beş neden yöntemlerini "yeterince titiz değil" olarak niteler; bu görüşü bir kaynakla desteklemez. Pratik bir okuma: basit yöntemler ekip tartışması için iyi başlangıç noktalarıdır ve karmaşık veya yüksek riskli arızalar daha titiz yöntemler gerektirebilir.

| Yöntem | Ne yapar | Ne zaman yardımcı olur |
|---|---|---|
| **Beş neden** | Bir belirtiden bir nedene doğru ilerlemek için tekrar tekrar "neden" sorar | Basit neden zincirlerinin hızlı, ekip düzeyinde tartışması |
| **Ishikawa (balık kılçığı) diyagramı** | Olası nedenleri kategoriye göre gruplar | Birçok olası nedeni beyin fırtınasıyla ortaya çıkarmak |
| **Pareto analizi** | Nedenleri sıklığa veya etkiye göre sıralar | Önce hangi tekrarlayan sorunun ele alınacağını seçmek |
| **Hata ağacı analizi** | Bir sonuca götüren arıza kombinasyonlarını haritalar | Güvenlik açısından kritik veya karmaşık arızalar |
| **FMEA** | Parçaların nasıl başarısız olabileceğine ve etkisinin ne olacağına ileriye dönük bakar | Proaktif tasarım gözden geçirmesi |

### Etkili düzeltici eylemler

Madde, yalnızca evrak işi veya eğitim ekleyen düzeltici eylemlerin daha az etkili olduğunu söyler. Pratikte bu, sistemi değiştiren eylemleri tercih etmeyi önerir: bir kontrolü otomatikleştirmek, bir arıza modunu ortadan kaldırmak, bir güvenlik önlemi eklemek, izlemeyi iyileştirmek. "Mühendislere dikkatli olmalarını hatırlat" gibi bir eylem zayıftır.

### Suçlamasızlık ilkesi

Sorun soruşturması, Google'ın SRE kitabında postmortem'ler için anlatılan suçlamasızlık ilkesini paylaşır: bireyleri suçlamadan katkıda bulunan nedenleri belirleyin, çünkü insanlar eğitilebilir ve sistemler düzeltilebilir (bkz. Konu 3.2 — Olay Yönetimi). "İnsan hatası" bulup duran bir soruşturma, genellikle çok erken durmuştur. Hatayı neyin mümkün kıldığını ve neyin onu zorlaştıracağını sorun.

### Çevik bir akışta sorun yönetimi

Pratik bir çevik yaklaşım şöyle görünür:

- Olaylar ve postmortem'ler aday sorunlar yaratır.
- Kısa, düzenli bir gözden geçirme tekrarlayan olayları gruplar ve sorunları etkiye ve sıklığa göre sıralar.
- Seçilen sorunlar, bir sahibi, bir hipotezi ve soruşturma için bir süre sınırıyla sıradan kalemler olarak iş listesine girer.
- Geçici çözümler, hizmet masasının ve nöbetçi mühendislerin kullanabilmesi için bilinen hatalar olarak kaydedilir (bkz. Konu 3.9 — Bilgi Yönetimi).
- Düzeltmeler küçüktür ve sınanmıştır, normal biçimde yayımlanır ve olayların durup durmadığını görmek için sonradan kontrol edilir.

## İyi uygulamalar

1. **Olayları sorunlara bağlayın.** Hangi olayların aynı nedene sahip göründüğünü kaydedin. Bağlantılar olmadan örüntüyü göremezsiniz ve örüntü olmadan bir düzeltme için tartışamazsınız.
2. **Olayları örüntüler için bir takvime göre gözden geçirin.** Ayda bir yakın zamandaki olayları hizmet ve olası nedene göre gruplayın ve en üstteki birkaçını seçin. Pareto düşüncesini kullanın: birkaç neden genellikle acının büyük bölümünü açıklar.
3. **Sorunları iş listesi kalemleri olarak görün.** Seçilen her soruna bir sahip, bir ifade ve soruşturma için bir süre sınırı verin ve diğer işlerle rekabet etmesine izin verin. Kimsenin zamanlamadığı ayrı bir "sorunlar" kuyruğu bir mezarlıktır.
4. **Net bir sorun ifadesiyle başlayın.** Ne olduğunu, nerede, ne sıklıkta olduğunu ve etkisinin ne olduğunu gerçekleri kullanarak yazın. Belirsiz ifadeler belirsiz düzeltmelere yol açar.
5. **Bir zaman çizelgesi oluşturun.** Normal işletimden arızaya kadar günlükleri, değişiklikleri ve etkinlikleri toplayın. Madde zaman çizelgesini temel bir adım olarak listeler ve birçok sürpriz kimsenin bağlamadığı değişikliklerden gelir.
6. **Ortadan kaldırıldığında yinelenmeyi önleyen nedeni sorun.** Maddenin sınamasını kullanın. Ekip bir neden önerdiğinde, onu ortadan kaldırmanın sorunun geri dönmesini durdurup durdurmayacağını sorun.
7. **Birden fazla neden bekleyin.** Tasarımda, izlemede, süreçte ve insanların bilgisinde katkıda bulunan etkenleri arayın. İlk makul olanda durmayın.
8. **Yöntemleri soruna uyacak şekilde seçin.** Hızlı ekip tartışması için beş neden veya balık kılçığı, ciddi veya karmaşık arızalar için daha titiz araçlar kullanın.
9. **Sistemi değiştiren eylemleri tercih edin.** Hatırlatmalar ve eğitim yerine otomasyonu, güvenlik önlemlerini ve daha iyi izlemeyi tercih edin. Kontrol edebilmek için beklenen etkiyi kaydedin.
10. **Geçici çözümleri bilinen hatalar olarak kaydedin.** Belirtinin nasıl göründüğünü, geçici çözümü ve düzeltmenin sahibini yazın. Kaydı hizmet masası ve nöbetçi personelle paylaşın.
11. **Düzeltmenin işe yaradığını kontrol edin.** Bir düzeltmeden sonra kararlaştırılan bir süre boyunca yinelenmeyi izleyin ve sonucu bildirin. Hiç kontrol edilmeyen bir düzeltme bir umuttur.
12. **Bulduklarınızı paylaşın.** Diğer ekiplerin benzer örüntüleri tanıyabilmesi için sorunların ve düzeltmelerin kısa özetlerini yayımlayın.

## Ekibinizle tartışılacak sorular

**Hangi olay hep geri geliyor ve nedeninin ne olduğunu düşünüyoruz?**

İnsanlardan en çok bıktıkları olayı adlandırmalarını isteyin. Yanıtları karşılaştırın. Ardından her kişinin nedenin ne olduğuna inandığını ve bunu nasıl bildiğini sorun. İnançlar çoğu zaman farklıdır; bu, ne kadar az ortak kanıt olduğunu gösterir. Kolaylaştırıcı, hangi verinin bunu çözeceğini sorabilir. Bir süre sınırıyla araştırılacak bir tane seçin.

**İki olayın aynı nedene sahip olup olmadığını nasıl bilebiliriz?**

Olayların nasıl kaydedildiğine bakın ve birinin ilgili olayları çabucak bulup bulamayacağını sorun. Tipik yanıtlar serbest metin, hafıza veya şanstır. Kayıtlarda hangi küçük değişikliğin yardımcı olacağını sorun; örneğin hizmet ve olası neden için bir alan. Birinde anlaşın.

**Bir gözden geçirmede "insan hatası" bulduğumuzda ne yapıyoruz?**

Yakın zamandan bir örnek isteyin. Soru, gözden geçirmenin orada durup durmadığıdır. Sistemde hatayı neyin mümkün kıldığını tartışın: belirsiz talimatlar, kafa karıştırıcı bir araç, zaman baskısı. İnsanları düzeltemeyeceğiniz ama sistemleri düzeltebileceğiniz fikriyle karşılaştırın. Her seferinde sorulacak bir soru üzerinde anlaşın; örneğin "Bunu yapmayı ne kolaylaştırdı?"

**Geçmiş gözden geçirmelerdeki hangi eylemler sistemi gerçekten değiştirdi ve hangileri yalnızca bir hatırlatma ekledi?**

Son beş gözden geçirmenin eylemlerini listeleyin ve her birini sistem değişikliği veya hatırlatma olarak işaretleyin. Madde, hatırlatmaların ve evrak işinin daha az etkili olduğunu söyler. Hatırlatmaların neden bu kadar yaygın olduğunu sorun: hızlı, ucuz ve eylem gibi hissettirirler. Daha güçlü bir düzeltmeyle değiştirilecek bir hatırlatma seçin.

**Kimsenin yazıya dökmediği geçici çözümlerimiz nerede?**

Nöbetçi mühendislere ve masa analistlerine hangi püf noktalarını kullandıklarını sorun. Yazılmamış her geçici çözüm bir risktir. Bunları belirti, geçici çözüm ve sahibiyle bilinen hatalar olarak kaydedin. Kolaylaştırıcı, her kayıttan kimin yararlandığını sorabilir. Bu hafta kısa bir liste yapın.

**Bir düzeltmenin işe yaradığını nasıl anlarız?**

Yakın zamandan bir düzeltme seçin ve bunu hangi kanıtın gösterdiğini sorun. Yanıt "artık şikâyet yok" ise ne kadar beklediğinizi ve neyi ölçtüğünüzü sorun. Basit bir kontrolü tartışın: belirli bir belirtiyi belirli bir süre boyunca izleyin. Kontrolü her düzeltmeyle kaydetmek üzere anlaşın.

## Uygulamada: çevik bir ITIL örneği

Orta ölçekli bir lojistik şirketi, sürücüleri ve sevk görevlilerinin kullandığı bir rota planlama hizmeti işletir. Dokuz kişilik platform ekibi, yaklaşık iki haftada bir aynı olayı ele almıştır: rota hesaplamaları sabahları on ila on beş dakika zaman aşımına uğrar ve sonra düzelir. Her seferinde nöbetçi mühendis bir işçi sürecini yeniden başlatır ve olay kapatılır. Sevk görevlileri sabah planlamasına güvenilemeyeceğinden yakınır.

Ekip lideri olayların aylık bir gözden geçirmesini başlatır; bunları hizmete ve olası nedene göre gruplar. Sabah zaman aşımları listenin başındadır. Olay kayıtlarından bir sorun ifadesi yazar: zaman aşımları hafta içi 7:00 ile 7:30 arasında gerçekleşir, on ila on beş dakika sürer ve tüm sevk görevlilerini etkiler. Ekip, 7:00'de zamanlanmış bir veri aktarımını ve aktarımın boyutunu artıran yakın zamanlı bir değişikliği içeren bir zaman çizelgesi oluşturur. Bir beş neden tartışması, aktarımın veritabanını doyurduğunu düşündürür. Bariz düzeltmeyi, kapasite eklemeyi denerler; ancak olaylar daha düşük bir oranda sürer ve kapasitenin kök değil, bir katkıda bulunan olduğu sonucuna varırlar.

İkinci bir bakış, aktarımın rota hesaplamalarının da okuduğu bir tabloyu kilitlediğini bulur. Ekip aktarımı ayrı bir kopyaya taşır ve kilit beklemeleri için bir uyarı ekler. Düzeltme canlıya çıkana kadar yeniden başlatmayı belirti ve geçici çözümle bilinen bir hata olarak kaydederler ve belirtiyi altı hafta boyunca izlemek üzere anlaşırlar. Olaylar durur. Bazı sorunlar kalır: bir ortaktan gelen bir başka aktarım hâlâ zirve zamanında çalışır ve ekip henüz ortağı takvimini değiştirmeye ikna edememiştir. Ortak takvimini bir sonraki planlama gündemine koyarlar ve kilit uyarısını yerinde tutarlar.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Nedenleri düzeltmenin bilgisi teslimat ekiplerindedir. En üstteki sorunları iş listenize alın ve bunları güven kazandıran iş olarak görün. Nedeni ortaya çıkaracak izleme ve testler ekleyin ve bilinen hatayı masanın kullanabileceği bir dille yazın.

### Hizmet ve operasyon ekipleri

Olayları operasyon ekipleri görür ve kayıtları tutar. Olayları bağlayın, aylık gözden geçirmeyi yürütün ve geçici çözümleri bilinen hatalar olarak kaydedin. Kanıtı teslimat ekiplerine, sıklık, etki ve zaman çizelgesiyle gerekçeyi oluşturan bir biçimde iletin.

### Liderlik ve yönetişim

Sorun düzeltmenin zaman bulup bulmayacağına liderler karar verir. En üstteki tekrarlayan sorunları ve bunlar hakkında ne yapıldığını isteyin. Onarımı ödüllendirdiği için kapatılan olay sayısını bir başarı ölçüsü olarak saymaya direnin. Çaba gerektiren ama acıyı ortadan kaldıran düzeltmeleri destekleyin.

### Müşteriler ve kullanıcılar

Tekrarlayan arızalar durduğunda müşteriler ve kullanıcılar yararlanır. Örüntüler ekibe yardımcı olduğundan, tekrarlayan sorunları tarihler ve etkilerle bildirin. Sağlayıcılara tekrarlayan kesintilerin nedenleri hakkında ne yaptıklarını sorun ve "yeniden başlattık"ın ötesinde bir yanıt bekleyin.

## Yaygın başarısızlık biçimleri

- **Ortadan kaldırmadan onarım.** Olaylar kapatılır ve geri döner. Bunun yerine tekrarları bir soruna bağlayın ve nedeni düzeltin.
- **Kimsenin zamanlamadığı bir sorun kuyruğu.** Sorunlar sonsuza kadar bekler. Bunun yerine seçilen sorunları sahiplerle ve süre sınırlarıyla iş listesine koyun.
- **İnsan hatasında durmak.** Gözden geçirme suçlanacak biriyle biter. Bunun yerine hatayı neyin mümkün kıldığını sorun ve sistemi düzeltin.
- **Zayıf eylemler.** Hatırlatmalar ve eğitim sistem değişikliklerinin yerini alır. Bunun yerine otomasyonu, güvenlik önlemlerini ve daha iyi izlemeyi tercih edin.
- **Tek bir kök neden aramak.** Ekip tek bir suçluda ısrar eder. Bunun yerine birkaç katkıda bulunan nedeni kabul edin ve en etkili olanları ele alın.
- **Düzeltmenin işe yaradığına dair kontrolün olmaması.** Sorun sürümde kapatılır. Bunun yerine belirtinin geri dönüp dönmediğini görmenin bir yolunu tanımlayın.
- **Yazılmamış geçici çözümler.** Bilgi bireylerde yaşar. Bunun yerine bilinen hataları kaydedin ve paylaşın.
- **Yöntem tapınması.** Ekipler tekniklerle ilgili tartışır. Bunun yerine yöntemleri soruna uyacak şekilde seçin ve çabayı kanıta harcayın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Bağlama ve önceliklendirme | Olaylar bağlanmaz | Bazı ekipler tekrarları not eder | Olaylar sorunlara bağlanır ve örüntüler için bir takvime göre gözden geçirilir | Sorunlar ölçülen etki ve sıklığa göre sıralanır | Sorun öncelikleri ekipler ve tedarikçiler arasında paylaşılır |
| Soruşturma | Soruşturma gayriresmîdir | Bazı ekipler basit yöntemler kullanır | Zaman çizelgeleri ve kanıtla yazılı bir yaklaşım kullanılır | Soruşturma kalitesi ve süresi gözden geçirilir | Soruşturmalar ortak verilerle ekipleri ve tedarikçileri kapsar |
| Düzeltici eylem | Düzeltmeler gelişigüzel veya hatırlatmadır | Bazı düzeltmeler sistemi değiştirir | Eylemler etkiye göre, sahipler ve tarihlerle seçilir | Etkiler kontrol edilir ve yinelenme ölçülür | Düzeltmeler kuruluş genelinde benzer sistemlere yayılır |
| Bilinen hatalar ve bilgi | Geçici çözümler yazılmamıştır | Bazıları bireyler tarafından kaydedilir | Bilinen hatalar kaydedilir ve masa ve nöbetçilerle paylaşılır | Bilinen hataların kullanımı ve doğruluğu izlenir | Bilinen hatalar kullanıcılar, tedarikçiler ve ortaklarla paylaşılır |

## Kontrol listesi

- [ ] Aynı nedeni paylaştığı görülen olaylar bağlanıyor.
- [ ] Düzenli bir gözden geçirme olayları grupluyor ve en üstteki tekrarlayan sorunları seçiyor.
- [ ] Seçilen sorunlar sahipleri ve süre sınırlarıyla iş listesinde.
- [ ] Her sorunun gerçeklerle yazılı bir ifadesi var.
- [ ] Her soruşturma için bir zaman çizelgesi oluşturuluyor.
- [ ] Gözden geçirmeler, herhangi bir insan hatasına sistemde neyin izin verdiğini soruyor.
- [ ] Eylemler, beklenen etki kaydedilerek hatırlatmalar yerine sistem değişikliklerini tercih ediyor.
- [ ] Geçici çözümler bilinen hatalar olarak kaydediliyor ve masa ile nöbetçi personelle paylaşılıyor.
- [ ] Her düzeltmenin kararlaştırılan bir süre boyunca yinelenme kontrolü var.
- [ ] Sorunların ve düzeltmelerin özetleri diğer ekiplerle paylaşılıyor.

## Yapay zeka istemleri

**Amaç: kayıtlarınızda tekrarlayan olayları ve aday sorunları bulmak.**

```text
Below are descriptions of [number] incidents from the last [period], with dates and the service affected: [paste anonymized descriptions, one per line].

Group the incidents that look as if they might share a cause, based only on what is written. For each group, list the incidents, give a one-sentence description of the common symptom, and say how confident you are and why (low, medium, high). List incidents that do not fit any group. Do not guess at technical causes beyond the text. Suggest three questions for the team to ask to test each group. List what you are unsure of.
```

**Amaç: kanıttan net bir sorun ifadesi yazmak.**

```text
Help me write a problem statement.

What we observe, with dates and counts: [paste facts].
What is affected and who is affected: [describe].
What we know about when it started and what changed around then: [paste, or write "unknown"].
What we have already tried: [paste].

Write a problem statement of three to five sentences that describes what happens, where, how often, and the impact, without naming a cause. Then list the facts we still need and where to find them. Mark anything that is an assumption. Do not suggest causes as facts. List what you are unsure of.
```

**Amaç: bir beş neden oturumuna hazırlanmak ve akıl yürütme zincirini kaydetmek.**

```text
Help me prepare a five whys discussion for this problem: [paste the problem statement].

Facts we have: [list evidence such as logs, timelines, and changes].

Prepare: a first "why" question grounded in the evidence, a template where each answer records the evidence for it, and a reminder to branch when there is more than one possible answer. Warn me against stopping at human error. After the session I will paste the notes: do not invent answers yourself. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: önerilen düzeltici eylemlerin sistemi değiştirip değiştirmediğini değerlendirmek.**

```text
Here are the actions proposed after our review: [paste a list].

For each, say whether it changes the system (for example automates a check, removes a failure mode, adds a safeguard, improves monitoring) or relies on people remembering or on training, and give one sentence of reasoning from the text only. For each reminder-type action, suggest a stronger alternative as a question for the team. Suggest how we could check whether each action worked, without inventing numbers. List what you are unsure of.
```

## Yapay zeka becerileri

- [root-cause-analysis](../../../../skills/root-cause-analysis/SKILL.md): bir soruşturmayı net bir sorun ifadesinden sınanmış bir nedene kadar yönlendirmek için kullanın.
- [fishbone-diagram](../../../../skills/fishbone-diagram/SKILL.md): bir ekiple olası nedenleri kategoriye göre beyin fırtınasıyla ortaya çıkarmak için kullanın.
- [cause-and-effect-diagram](../../../../skills/cause-and-effect-diagram/SKILL.md): karmaşık bir arızada nedenlerin ve etkilerin nasıl bağlandığını ortaya koymak için kullanın.
- [postmortem](../../../../skills/postmortem/SKILL.md): aday sorunları belirleyen gözden geçirmeyi yürütmek için kullanın.
- [six-sigma](../../../../skills/six-sigma/SKILL.md): değişkenliği veya tekrarlayan kusurları çözümlemek için veriye dayalı yöntemlere ihtiyaç duyduğunuzda kullanın.

## Temel kaynaklar

- **Root cause analysis** (Wikipedia): yöntemlere dair ISO/IEC 31010'un listelendiği, yöntemin, ilkelerin ve sınırların genel bir özeti.
- **Postmortem Culture: Learning from Failure** (*Site Reliability Engineering*, Google, sre.google): arızalardan öğrenmeye yönelik suçlamasız yaklaşım.
- **Managing Incidents** (*Site Reliability Engineering*, Google, sre.google): olay ele almanın sonraki çözümlemeyi nasıl beslediği.
- **Ishikawa diagram** ve **Five whys** (Wikipedia): iki yaygın basit yöntem hakkında arka plan.

## Kaynakça

1. Root cause analysis — Wikipedia — https://en.wikipedia.org/wiki/Root_cause_analysis
2. Postmortem Culture: Learning from Failure — Google SRE book, sre.google — https://sre.google/sre-book/postmortem-culture/
3. Managing Incidents — Google SRE book, sre.google — https://sre.google/sre-book/managing-incidents/
4. Five whys — Wikipedia — https://en.wikipedia.org/wiki/Five_whys
5. Ishikawa diagram — Wikipedia — https://en.wikipedia.org/wiki/Ishikawa_diagram
6. Failure mode and effects analysis — Wikipedia — https://en.wikipedia.org/wiki/Failure_mode_and_effects_analysis
7. Fault tree analysis — Wikipedia — https://en.wikipedia.org/wiki/Fault_tree_analysis
8. Pareto analysis — Wikipedia — https://en.wikipedia.org/wiki/Pareto_analysis
9. Incident management — Wikipedia — https://en.wikipedia.org/wiki/Incident_management
10. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
