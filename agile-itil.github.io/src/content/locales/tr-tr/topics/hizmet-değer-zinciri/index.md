# Hizmet Değer Zinciri

**Hizmet değer zinciri, ekiplerin değer akışları oluşturmak için farklı sıralarla birleştirdiği altı etkinlik kümesidir ve sürekli teslimat ile hizmet işletiminin iki ayrı akış yerine tek bir akışa nasıl sığdığını anlatır.**

## Bu neden önemli

Birçok kuruluş geliştirmeyi ve işletmeyi iki aşama olarak görür: önce bir proje hizmeti oluşturur, sonra bir operasyon grubu onu devralır. Devir teslim, bilginin kaybolduğu, sorumluluğun bulanıklaştığı ve müşterilerin boşluğu hissettiği yerdir. ITIL 4 hizmet değer zinciri, bu tabloyu, aynı etkinliklerin duruma bağlı olarak herhangi bir sırayla ve gerektiği kadar sık gerçekleşebildiği bir tabloyla değiştirmek üzere tasarlanmıştır.

Bu, çevik ekiplerin zaten çalışma biçimine yakındır. Bir hafta içinde bir ekip bir özelliği planlayabilir, bir kısmını geliştirebilir, yayımlayabilir, bir müşterinin bu konudaki sorusunu yanıtlayabilir ve üretimde bulunan bir sorunu düzeltebilir. Bunların her biri zincirde farklı bir etkinliktir. Bunları tek bir akışın parçaları olarak görmek, bir ekibin işin nerede beklediğini, her etkinliği kimin yaptığını ve hangi etkinliklerin ihmal edildiğini sormasına yardımcı olur.

Bu konu altı etkinliği, bunların değer akışlarına nasıl birleştiğini ve çevik bir ekibin bu fikri nasıl kullanabileceğini anlatır. Özetler bir eğitim sağlayıcısından ve bir yazılım tedarikçisinden gelir; çünkü bu kılavuz için okunan çerçeve sahibinin herkese açık sayfaları hizmet değer zincirinden yalnızca geçerken söz eder. Tedarikçi sayfası etkinlikleri anlatmadan listeler; bu nedenle aşağıdaki açıklamaları yaygın kullanılan okumalar olarak görün ve sahibin ifadesi için ITIL 4 yayınlarına bakın (bkz. Konu 2.2 — ITIL).

## Temel kavramlar

### Zincirin yeri

Hizmet değeri sisteminde zincir, merkezdeki işletim modelidir (bkz. Konu 2.3 — ITIL Hizmet Değeri Sistemi). Bir tedarikçi sayfası bunu, bir ürün veya hizmetin teslimat hattı ya da yaşam döngüsüyle ilgili sistem parçası olarak anlatır; girdi olarak talebi alır ve çıktı olarak değer üretir. Ayrıca uygulamada yaşam döngüsünün nadiren doğrusal olduğunu not eder.

### Altı etkinlik

Tablo her etkinliği, bir eğitim sağlayıcısının sayfasının onun için belirttiği amacı ve etkinliğin çevik bir ekipte nasıl görünebileceğini verir. Sağ sütun bu kılavuzun okumasıdır.

| Etkinlik | Bir eğitim sağlayıcısının özetlediği amaç | Çevik bir ekipte nasıl görünebilir |
|---|---|---|
| **Planla** | Kuruluşun yönü için politikaları, hedefleri ve yönergeleri tanımlar; böylece herkes vizyon, mevcut durum ve iyileştirme yönü konusunda ortak bir anlayışa sahip olur | Ürün hedefleri, yol haritaları, çeyreklik planlama ve portföy seçimleri |
| **İyileştir** | Tüm etkinlikler boyunca hizmetleri, uygulamaları ve süreçleri sürekli iyileştirir | Retrospektifler, olay sonrası gözden geçirmeler ve iş listesindeki iyileştirme kalemleri |
| **Etkileşim kur** | İhtiyaçları anlamak, bilgi vermek, geri bildirim ve gereksinim toplamak ve ilişkileri yönetmek için paydaşlarla etkileşir | Kullanıcı araştırması, sprint gözden geçirmeleri, hizmet masası ve müşteri görüşmeleri |
| **Tasarla ve geçiş yap** | Yeni veya değiştirilmiş hizmetlerin, tasarımdan canlı ortama kadar paydaşların beklentilerini karşılamasını sağlar | Bir değişikliği tasarlamak, sınamak ve sürüm ile destek için hazırlamak |
| **Edin/geliştir** | Fiziksel kaynaklar, altyapı, bilgi veya yazılım gibi hizmetler için gereken bileşenleri edinir veya oluşturur | Yazılım geliştirmek, bir araç satın almak, altyapıyı hazırlamak, personeli eğitmek |
| **Sun ve destekle** | Hizmetleri üzerinde anlaşıldığı gibi sunar ve sorunları çözmek ve talepleri karşılamak için süregiden destek sağlar | Hizmeti işletmek, olayları ve talepleri ele almak, sürümleri dağıtmak |

### Etkinlikler aşama değildir

Eğitim sağlayıcısının sayfası, etkinliklerin "doğrusal olmadığını, birbirine bağlı olduğunu ve birden çok değer akışı oluşturmak üzere çeşitli biçimlerde birleştirilebileceğini" söyler. **Değer akışı** onun sözleriyle, müşterilere belirli bir hizmeti veya ürünü oluşturan ve sunan belirli bir etkinlikler kümesidir. Merkezî fikir budur. Zincir bir etkinlik menüsüdür ve bir değer akışı, belirli bir amaç için seçilmiş ondan geçen bir yoldur.

### Örnek değer akışları

Bu kılavuz için okunan sayfalar örnek değer akışı vermez; bu nedenle aşağıdakiler, etkinliklerin nasıl birleşebileceğine dair bu kılavuzun örneklemeleridir. ITIL yayınlarından değildir ve gerçek bir akış farklı olacaktır.

| Değer akışı | Etkinlikler arasında olası bir yol |
|---|---|
| **Bir olayı ele almak** | Etkileşim kur (bir kullanıcı bildirir) → sun ve destekle (hizmeti geri getir) → iyileştir (nedeni gözden geçir ve düzelt) |
| **Bir özelliği yayımlamak** | Planla (hedefe karar ver) → tasarla ve geçiş yap (tasarla, sına, desteği hazırla) → edin/geliştir (geliştir) → sun ve destekle (yayımla) → etkileşim kur (geri bildirim al) → iyileştir |
| **Bir erişim talebini karşılamak** | Etkileşim kur (talep alındı) → sun ve destekle (erişimi kontrol et ve ver) → etkileşim kur (kullanıcıyla doğrula) |
| **Yeni bir tedarikçiyi devreye almak** | Planla (ihtiyaca karar ver) → etkileşim kur (koşulları seç ve üzerinde anlaş) → edin/geliştir (entegre et) → sun ve destekle (işlet) → iyileştir (performansı gözden geçir) |

### Uygulamalar ve zincir

Uygulamalar, etkinliklerin başvurduğu yetkinliklerdir. Örneğin olay yönetimi, birkaç değer akışında kullanılan bir uygulamadır. Kaynaklar uygulamalar ile etkinlikler arasındaki eşleştirmenin her ayrıntısında hemfikir değildir; bu nedenle katı bir tablodan kaçının. Daha iyi bir sınama, bir uygulamanın incelediğiniz değer akışına katkıda bulunup bulunmadığıdır (bkz. 3. Bölüm).

### Değer akışları ve çevik akış

Çevik ve yalın düşünce zaten değer akışlarını kullanır (bkz. Konu 1.7 — Yalın Yazılım Geliştirme). Bir değer akışı haritası, bir yoldaki adımları, süreleri ve beklemeleri gösterir. ITIL fikri, adımları sınıflandırmak için bir sözcük dağarcığı ve yolun geliştirmenin yanı sıra destek ve iyileştirmeyi de içerdiğine dair bir hatırlatma ekler. Dijital iş için bu, değer akışı yönetimine bağlanır (bkz. Konu 5.4 — Değer Akışı Yönetimi).

### Sınırlar

Bu kılavuz için okunan sayfalar değer akışlarını tasarlamak veya seçmek için bir yöntem vermez ve tedarikçi sayfası, iyileştirmeyi hayati olarak adlandırmanın ötesinde zincirin sürekli iyileştirmeyle nasıl ilişkili olduğunu açıklamaz. Zincir, işi tanımlamanın bir yoludur; nasıl yapılacağına karar vermenin yolu değil. Değeri, gerçek akışlara bakmak için kullanıp kullanmadığınıza bağlıdır.

## İyi uygulamalar

1. **Bir değer akışı seçin ve çizin.** Bir değişikliği yayımlamak veya bir talebi ele almak gibi müşteriler için önemli bir akış seçin. Adımları sırayla listeleyin ve her birini altı etkinlikten en yakın olanla etiketleyin.
2. **Destek ve iyileştirmeyi resme dâhil edin.** Akışı sürümde bitirmeyin. Sonrasında olanları gösterin: olayları ele almak ve onlardan öğrenmek.
3. **Eksik etkinlikleri arayın.** Bir akışta etkileşim kurma adımı yoksa kimse kullanıcılarla konuşmuyordur. İyileştirme adımı yoksa hiçbir şey öğrenilmiyordur. Önemli oldukları yerlerde ekleyin.
4. **Beklemeleri zamanlayın.** Bir akış için işin etkinlikler arasında ne kadar beklediğini ve bir ekip sınırını nerede geçtiğini kaydedin. En uzun bekleme, incelenecek ilk şeydir (bkz. Konu 5.4 — Değer Akışı Yönetimi).
5. **Etkinlikleri özgürce birleştirin.** Farklı akışların farklı yollar kullanmasına izin verin. Küçük bir hatanın düzeltmesi, bir planlama adımı olmadan doğrudan sun ve destekle'den edin/geliştir'e gidip geri dönebilir.
6. **Tasarla ve geçiş yap'ı ekibin işine koyun.** Destek notlarını, izlemeyi ve eğitimi, sonda bir devir teslim olarak değil, geliştirmenin bir parçası olarak dâhil edin (bkz. Konu 3.5 — Sürüm ve Dağıtım Yönetimi).
7. **"Etkileşim kur"u sürekli bir etkinlik yapın.** Kullanıcılarla teması bir projenin başı ve sonuyla sınırlamayın. Hizmet masasını ve müşteri geri bildirimini planlamaya dâhil edin.
8. **Planlamayı operasyondan gelen kanıtlara bağlayın.** Hedeflerin kullanıcıların gerçekte deneyimlediğini yansıtması için planlama konuşmalarında olay ve talep verilerini kullanın (bkz. Konu 5.1 — Çevik Hizmet Yönetimi).
9. **Her akış için bir sahip adlandırın.** Bir kişi akışın nasıl performans gösterdiğini söyleyebilmeli ve ekipleri onu iyileştirmek için bir araya getirebilmelidir.
10. **Zinciri boşluklar için bir kontrol listesi olarak kullanın.** Bir şey başarısız olduğunda hangi etkinliğin zayıf olduğunu sorun: belirsiz plan, zayıf etkileşim, aceleye getirilmiş geçiş, zayıf geliştirme, sallantılı destek veya iyileştirme yokluğu.
11. **Diyagramı basit tutun.** Altı etiketli kaba bir çizim yeterlidir. Çizim bir göstergeye ihtiyaç duyuyorsa basitleştirin.
12. **Akışları değişikliklerden sonra gözden geçirin.** Ekip yapıları, tedarikçiler veya araçlar değiştiğinde akışların çizildiği gibi hâlâ çalışıp çalışmadığını kontrol edin.

## Ekibinizle tartışılacak sorular

**Kullanıcılarımız için en önemli üç değer akışı hangileri ve her birinin sahibi kim?**

İnsanlardan en çok önem taşıyan akışları, örneğin bir kullanıcının yeni bir hesap alması veya bir düzeltmenin üretime ulaşması gibi, adlandırmalarını isteyin. Listeleri karşılaştırın. Farklılıklar ekibin neyin önemli olduğuna dair farklı resimlere sahip olduğunu gösterir. Kolaylaştırıcı, her akış için uçtan uca kimin yanıt verebileceğini sorabilir. Çoğu zaman kimse veremez; bu bir bulgudur.

**Bir akış için altı etkinlikten hangilerini iyi yapıyoruz ve hangilerini atlıyoruz?**

Akışı çizin ve adımları etiketleyin. Ardından eksik etkinlikleri arayın. Ekipler çoğu zaman iyi planladıklarını ve geliştirdiklerini, ancak kötü etkileşim kurup iyileştirdiklerini görür. Eksik etkinliğin ne katacağını ve neye mal olacağını sorun. Küçük ölçekte eklenecek bir tane seçin.

**İş etkinlikler arasında nerede bekliyor ve beklemenin sahibi kim?**

Devir teslimleri işaretleyin ve tipik beklemeleri not edin. Birçok bekleme ekipler arasındaki sınırda yer alır. Beklemenin, bir risk kontrolü gibi gerekli mi yoksa ekiplerin örgütlenme biçiminin bir kazası mı olduğunu sorun. Kısaltılacak bir tane seçin.

**Kullanıcıların teslim ettiklerimiz hakkında ne düşündüğünü nasıl öğreniyoruz ve bu planlarımızı ne kadar çabuk değiştiriyor?**

Yakın zamandan bir geri bildirimi kullanıcıdan iş listesine kadar izleyin. Adımları sayın. Haftalar sürdüyse ya da hiç ulaşmadıysa etkileşim kurma etkinliği zayıftır. Yolu neyin kısaltacağını sorun; örneğin hizmet masasıyla ortak bir kanal. Bir değişiklik üzerinde anlaşın.

**Bir sonraki olayı veya sürümü iyileştirmek için bir olaydan veya sürümden sonra ne yapıyoruz?**

Son birkaç olay ve sürüm için kaydedilmiş bir iyileştirme olup olmadığına bakın. Yoksa iyileştirme etkinliği gayriresmîdir. İyileştirme eylemlerinin sahibinin kim olduğunu ve nasıl izlendiğini sorun. Bunları kaydetmek için basit bir yer üzerinde anlaşın.

**Hangi akışlar kuruluş sınırlarını aşıyor ve bütün adına kim konuşuyor?**

Tedarikçileri, diğer departmanları veya müşterileri kapsayan akışları listeleyin. Uçtan uca akıştan kimin sorumlu olduğunu ve sınırlarda ne olduğunu sorun. İyi bir sonuç, bir koordinatör ve sınır ötesinde düzenli bir görüşme adlandırmaktır.

## Uygulamada: çevik bir ITIL örneği

Bölgesel bir hastane grubu, randevu almak ve test sonuçlarını görmek için kullanılan bir hasta portalı hizmeti işletir. On kişilik bir ekip bunu geliştirir ve işletir. Ekip her iki haftada bir yeni özellikler yayımlar, ancak hastalar bildirilen arızaların düzeltmelerinin aylar sürdüğünden ve geri bildirim mesajlarına yanıt alamadıklarından yakınır.

Dijital hizmetler başkanı ekipten, hastanın mesajından üretimdeki bir düzeltmeye kadar bildirilen bir arıza için değer akışını çizmesini ister. Adımları altı etkinlikle etiketlerler. Mesaj bir iletişim formuyla gelir (etkileşim kur) ve kimse önceliklendirmeden önce günlerce paylaşılan bir gelen kutusunda bekler. Önceliklendirilen bir arıza, yeni özelliklerle aynı iş listesine (planla) girer ve orada kötü rekabet eder. Bir düzeltme geliştirilir (edin/geliştir), sınanır ve bir sonraki özellik grubuyla yayımlanır (tasarla ve geçiş yap, sun ve destekle). Kimse hastaya söylemez (etkileşim kur) ve kimse arızanın ekibe ne öğrettiğini kaydetmez (iyileştir).

Ekip akışı değiştirir. Paylaşılan gelen kutusu bir nöbet çizelgesiyle her gün kontrol edilir, arızalar etiketlenir ve iş listesinde bir sonraki sürümü hedefleyen ayrı bir şerit verilir, hasta alındığında bir yanıt ve düzeltme canlıya çıktığında bir yanıt daha alır ve bir aydan eski her arıza iki haftalık gözden geçirmede tartışılır. İki ay sonra düzeltme süresinin medyanı düşer ve hastaların sessizlik hakkındaki şikâyetleri azalır. Sorunlar kalır: bir tedarikçi tarafından işletilen hastanenin randevu sistemini kapsayan arızalar hâlâ tedarikçinin kuyruğunu bekler ve yanıt mesajları geliştiriciler tarafından, bazı hastaların takip etmesini zor bulduğu bir dille yazılır. Ekip tedarikçiyi gözden geçirmeye davet eder ve iletişim ekibinden sade dilli şablonlar hazırlamasını ister.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri genellikle çoğu zamanı planla, tasarla ve geçiş yap ve edin/geliştir etkinliklerine harcar. Diğer üçüne bakın: kullanıcılarla nasıl etkileşim kurduğunuza, yayımladığınızı nasıl desteklediğinize ve nasıl iyileştirdiğinize. Destek taleplerini ve olay öğrenimini planlamaya girdi olarak görün.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri çoğu zamanı sun ve destekle ile etkileşim kurun'un bazı kısımlarına harcar. Zinciri, işinizin tasarla ve geçiş yap gibi önceki etkinliklere nasıl bağlı olduğunu göstermek ve onlardan ihtiyaç duyduğunuzu istemek için kullanın. Operasyon bilgisinin akışın başına ulaşması için planlamaya katılın.

### Liderlik ve yönetişim

Liderler, önemli hizmetler için akışın nerede koptuğunu sormak amacıyla zinciri kullanabilir. Akış sahiplerinin adlandırılmasını destekleyin ve onlara ekipleri bir araya getirme yetkisi verin. Altı etkinliği altı departmana dönüştürmekten kaçının; amaç onları birbirine bağlamaktır.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar esas olarak etkileşim kurmaya katılır ve geri bildirim planlara ve düzeltmelere kadar ulaştığında yararlanır. Yanıt ve görünür sonuç bekleyin. Sağlayıcıya sizin için hangi akışın en önemli olduğunu ve hangi gecikmelerin size zarar verdiğini söyleyin.

## Yaygın başarısızlık biçimleri

- **Zinciri bir dizi olarak okumak.** Ekipler her işi altısından sırayla geçirmeye zorlar. Bunun yerine işe uyan yollar seçin.
- **Akışları değil, departmanları haritalamak.** Her etkinlik bir departmana atanır ve akış kaybolur. Bunun yerine tek bir işi bunlar boyunca izleyin.
- **Etkileşim kur ve iyileştir'i unutmak.** Akış sürümde biter. Bunun yerine her akışa kullanıcı temasını ve öğrenmeyi dâhil edin.
- **Tasarla ve geçiş yap yerine devir teslim.** Destek notları, izleme ve eğitim sona bırakılır. Bunun yerine bunları baştan işin içine yerleştirin.
- **Akış sahibinin olmaması.** Kimse bir akışın nasıl performans gösterdiğini söyleyemez. Bunun yerine ekipleri toplama yetkisi olan bir sahip adlandırın.
- **Aşırı ayrıntılı diyagramlar.** Harita kimsenin okumadığı bir afişe dönüşür. Bunun yerine bir sayfada tutun ve bir şey değiştiğinde güncelleyin.
- **Sözcük dağarcığını amaç saymak.** Ekipler iyileştirmek yerine etiketlemeye zaman harcar. Bunun yerine yalnızca bir boşluğu bulmaya yardımcı olanı etiketleyin.
- **İkincil özetlere güvenmek.** Etkinliklerin açıklamaları kaynaklar arasında farklıdır. Bunun yerine kesinlik önemli olduğunda sahibinin yayınlarını kontrol edin.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Değer akışı görünürlüğü | Akışlar yalnızca gayriresmî olarak bilinir | Bazı akışlar ekipleri tarafından çizilmiştir | Kilit akışlar sahipleriyle haritalanmıştır | Akışlar bekleme ve sonuçlar bakımından ölçülür | Akışlar kuruluş sınırlarını aşar ve birlikte iyileştirilir |
| Etkinlik kapsamı | Planlama ve geliştirme baskındır | Bazı ekipler etkileşim kur ve iyileştir etkinliklerini ekler | Altı etkinliğin tümü kilit akışlarda görünür | Kapsam boşlukları izlenir ve kapatılır | Kapsam, kanıta dayanarak ekipler ve tedarikçiler arasında dengelenir |
| Devir teslimler ve geçiş | Devir teslimler geç ve yönetimsizdir | Bazı ekipler desteği geliştirmeye dâhil eder | Destek, izleme ve eğitim her sürümün parçasıdır | Geçiş sorunları ölçülür ve azaltılır | Geçiş teslimat, operasyon ve tedarikçiler arasında paylaşılır |
| Geri bildirim ve iyileştirme | Geri bildirim şikâyetle gelir | Bazı geri bildirimler iş listesine ulaşır | Geri bildirim ve iyileştirme kalemleri sahipleriyle izlenir | İyileştirmelerin etkileri denetlenir | Geri bildirim ve öğrenme ekipler ve müşteriler arasında sürekli akar |

## Kontrol listesi

- [ ] Kullanıcılar için önemli olan en az bir değer akışı çizdik.
- [ ] Çizimdeki her adım en yakın değer zinciri etkinliğiyle etiketlendi.
- [ ] Akış, kullanıcılarla etkileşimi ve iyileştirmeleri kaydeden bir adımı içeriyor.
- [ ] İşin nerede ve ne kadar beklediğini, en azından kabaca biliyoruz.
- [ ] İzleme ve destek notları gibi tasarla ve geçiş yap çalışması geliştirmenin parçasıdır.
- [ ] Adlandırılmış bir kişi akışın uçtan uca akışına sahiptir.
- [ ] Kullanıcılardan gelen geri bildirim iş listesine ulaşıyor ve yanıt alıyor.
- [ ] Olay ve talep verileri planlamada kullanılıyor.
- [ ] Akış, önemli değişikliklerden sonra gözden geçiriliyor.
- [ ] Her etkinliğin tam tanımı için sahibinin yayınını kontrol ettik.

## Yapay zeka istemleri

**Amaç: gerçek bir akışın adımlarını altı etkinlikle etiketlemek.**

```text
Help me label the steps of a value stream with the six ITIL service value chain activities: plan; improve; engage; design and transition; obtain/build; deliver and support.

The stream (what it delivers and to whom): [describe].
The steps in order, with who does each and how long it waited before it, if known: [paste].

For each step, suggest the closest activity and give one sentence of reasoning using only my text. Then list which of the six activities do not appear, and what that might mean, as questions and not conclusions. Do not invent steps or durations. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Amaç: geri bildirimin iş listesine giderken nerede kaybolduğunu bulmak.**

```text
I want to trace how user feedback reaches our backlog.

Where feedback arrives (channels): [list].
What happens to a piece of feedback after it arrives, step by step, with who does each step: [paste].
One recent example, with dates: [paste].

Describe the path in order and identify steps where the feedback could be lost or delayed, using only my text. Suggest three questions for the people involved and one small change to shorten the path. Do not invent causes. Ask clarifying questions first if information is missing, and list what you are unsure of.
```

**Amaç: teslimat ve operasyon personeliyle bir değer akışı çalıştayı planlamak.**

```text
Plan a 90-minute workshop for [number] people from delivery and operations to draw one value stream: [stream name].

Preparation: they will bring [data, such as dates of recent examples].
Constraints: [for example remote, different time zones].

Give a timed agenda, instructions for drawing the stream step by step, how to label steps with the six value chain activities, a way to mark waits and handovers, and a closing step to agree one change with an owner and date. Keep it free of any particular tool. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: yeni ekip üyeleri için değer zincirine dair kısa bir rehber yazmak.**

```text
Write a one-page guide to the ITIL service value chain for new team members.

Use only these notes, which I verified: [paste the six activity names and the descriptions you have checked against official sources, plus any examples from our own work].

Include: what the chain is for, one example stream from our work, and three questions a new person can ask to find which activity a task belongs to. Keep the language plain. Do not add claims about ITIL beyond my notes. Mark assumptions, and list what you are unsure of.
```

## Yapay zeka becerileri

- [value-stream-map](../../../../skills/value-stream-map/SKILL.md): bir akışı çizmek, beklemelerini zamanlamak ve adımlarını etiketlemek için kullanın.
- [workflow-analysis](../../../../skills/workflow-analysis/SKILL.md): işin roller arasında nasıl hareket ettiğini çözümlemek ve devir sorunlarını bulmak için kullanın.
- [agile-delivery](../../../../skills/agile-delivery/SKILL.md): bir ekibin geliştirme ve sürüm etkinlikleri boyunca küçük adımlarla nasıl teslim edeceğini planlamak için kullanın.
- [getting-feedback](../../../../skills/getting-feedback/SKILL.md): etkileşim kur etkinliği için kullanıcılardan geri bildirim toplama yollarını tasarlamak için kullanın.
- [agile-reflection](../../../../skills/agile-reflection/SKILL.md): iyileştir etkinliğini gerçek kılan gözden geçirmeleri yürütmek için kullanın.

## Temel kaynaklar

- **ITIL 4 Foundation** (PeopleCert): hizmet değer zincirini çalışılan konular arasında adlandıran sahibin sayfası.
- **ITIL service value system** (Purple Griffon): bir eğitim sağlayıcısının altı etkinliğin ve değer akışlarının özeti; ikincil.
- **The ITIL 4 Service Value System** (ManageEngine): etkinlikleri adlandıran bir tedarikçi özeti; ikincil.
- **Value-stream mapping** (Wikipedia): yalın uygulamanın israfı bulmak için kullandığı haritalama tekniği hakkında arka plan.

## Kaynakça

1. ITIL 4 Foundation — PeopleCert — https://www.peoplecert.org/browse-certifications/it-governance-and-service-management/ITIL-1/itil-4-foundation-2565
2. ITIL service value system — Purple Griffon (training provider; secondary source) — https://purplegriffon.com/blog/itil-service-value-system
3. The ITIL 4 Service Value System — ManageEngine (software vendor; secondary source) — https://manageengine.com/products/service-desk/itsm/itil-4-service-value-system.html
4. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
5. Value-stream mapping — Wikipedia — https://en.wikipedia.org/wiki/Value-stream_mapping
6. Value chain — Wikipedia — https://en.wikipedia.org/wiki/Value_chain
7. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
8. Business process management — Wikipedia — https://en.wikipedia.org/wiki/Business_process_management
9. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
