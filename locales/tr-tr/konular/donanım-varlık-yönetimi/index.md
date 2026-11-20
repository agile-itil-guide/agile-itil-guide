# Donanım Varlık Yönetimi

**Donanım varlık yönetimi fiziksel ekipmanı satın almadan elden çıkarmaya kadar izler; sessiz riskleri ise kimsenin bilmediği cihaz, çok uzun süre tutulan cihaz ve üzerinde hâlâ veri varken ayrılan cihazdır.**

## Bu neden önemli

Önce bulut yaklaşımının hâkim olduğu bir dünyada bile donanım önemlidir. İnsanlar dizüstü bilgisayarlarda, telefonlarda ve tabletlerde çalışır. Ağlar anahtarlar (switch) ve erişim noktaları üzerinde çalışır. Birçok kuruluş sunucuları, depolamayı ve özel ekipmanı yerinde tutar. Bir dizüstü bilgisayar kaybolduğunda, bir sunucunun garantisi bittiğinde veya bir cihaz partisinin değiştirilmesi gerektiğinde sorular aynıdır: neyimiz var, nerede, kimde, değeri ne ve neyi barındırıyor?

Kötü donanım yönetimi tanıdık biçimlerde ortaya çıkar. Depoda ne olduğunu kimse bilmediği için çalışanlar ekipman bekler. Eski cihazlar, değiştirilmelerini haklı çıkaracak veri olmadığı için hizmette kalır ve sonra uygunsuz bir anda bozulur. Cihazlar üzerlerinde hâlâ veri varken atılır. Garanti talepleri kaçırılır. Çevik bir ekip için bunun etkisi yavaşlayan işe alıştırma, bakımsız test donanımında başarısız sürümler ve hiçbir hattın göremediği güvenlik açıklarıdır.

[Wikipedia'daki BT varlık yönetimi bölümü](https://en.wikipedia.org/wiki/IT_asset_management), ki veri merkezi yönetimi maddesinin içinde yer alır, donanım varlık yönetimini bilgisayar ve ağ bileşenlerinin edinilmesinden elden çıkarılmasına kadar olan süreci kapsayan; talep ve onay, satın alma, yaşam döngüsü yönetimi, yeniden konuşlandırma ve elden çıkarma uygulamalarını içeren bir uygulama olarak tanımlar ve yaşam döngüsü boyunca mali bilginin yakalanmasının temel bir bileşen olduğunu söyler. Kısadır. Bu konu, elden çıkarma için elektronik atık ve veri silme maddelerini, bir de yaygın uygulamadan alınan pratik rehberliği ekler ve bunu yaptığı yerde belirtir.

## Temel kavramlar

### Kapsam

Donanım varlıkları son kullanıcı cihazlarını (dizüstü bilgisayarlar, masaüstü bilgisayarlar, telefonlar, tabletler), sunucuları ve depolamayı, ağ ekipmanını, çevre birimlerini ve özel ya da operasyonel teknolojiyi içerir. Bunları kullanılabilir kılan aksesuarları da kapsar. Her biri için kuruluş temel bilgileri bilmek ister: ne olduğu, kimin sorumlu olduğu, nerede olduğu, maliyetinin ne olduğu ve hangi durumda olduğu.

### Donanım yaşam döngüsü

Wikipedia bölümü talep ve onay, satın alma, yaşam döngüsü yönetimi, yeniden konuşlandırma ve elden çıkarmayı sıralar. Yaygın biçimde kullanılan ve burada da öyle sunulan pratik bir genişletme:

| Aşama | Yanıtlanacak sorular | Tipik kayıtlar |
|---|---|---|
| **Talep ve onay** | Neye ihtiyaç var ve kim onaylıyor? | Talep, onay, bütçe kodu |
| **Satın alma** | Ne aldık, kimden, hangi koşullarla? | Sipariş, fatura, garanti, tedarikçi |
| **Teslim alma ve hazırlama** | Geldi mi? Yapılandırıldı ve etiketlendi mi? | Seri numarası, varlık etiketi, yapılandırma |
| **Atama ve işletme** | Kimde? Ne için kullanılıyor? | Sahip veya kullanıcı, konum, desteklenen hizmet |
| **Bakım** | Durumu, garantisi ve yama durumu nedir? | Onarımlar, garanti bitişi, bellenim (firmware) durumu |
| **Yeniden konuşlandırma** | Başkası kullanabilir mi? | Silme, yeniden atama kaydı |
| **Emekliye ayırma ve elden çıkarma** | Veriler kaldırıldı mı? Nereye gitti? | Silme kanıtı, elden çıkarma kaydı |

### Mali bilgi

Wikipedia bölümü donanım yaşam döngüsüne ilişkin mali bilginin yakalanmasını vurgular. Yararlı bilgiler arasında satın alma maliyeti, amortisman, garanti ve destek maliyeti ile çalışır durumda tutma maliyeti vardır. Bunlar değiştirme kararlarını ve bütçeleri besler (bkz. Konu 4.5 — BT Mali Yönetimi ve FinOps). Desteklenmesi değiştirilmesinden daha pahalı olan bir cihaz emekliye ayırma adayıdır.

### Değiştirme ve yenileme

Kuruluşlar ekipmanı genellikle bir döngüyle, örneğin dizüstü bilgisayarlar için birkaç yılda bir değiştirir. Bu kılavuz için okunan kaynaklar önerilen süreler belirtmez ve doğru aralık ekipmana, işe ve arıza maliyetine bağlıdır. Veriye dayalı bir yaklaşım arıza oranlarına, destek maliyetine, güvenlik desteğine ve performansa bakar ve kanıt gerektirdiğinde değiştirir. Sabit bir döngüyü planlamak daha kolaydır; kanıta dayalı bir döngü ise para tasarrufu sağlayabilir veya arızaları önleyebilir.

### Kullanım ömrü sonunda veri güvenliği

Elden çıkarma, donanım yönetiminin bilgi güvenliğiyle buluştuğu yerdir (bkz. Konu 3.13 — Bilgi Güvenliği Yönetimi). Wikipedia'daki veri silme maddesi veri silmeyi, saklanan verinin kurtarılamaz olması için bir sürücünün her sektörünün üzerine yazan bir yazılım yöntemi olarak anlatır; olağan dosya silme yalnızca işaretçileri kaldırır ve yaygın araçlar veriyi çoğu zaman geri getirebilir. Maddeden temel noktalar:

- **Üzerine yazma** sürücüyü kullanılabilir bırakır. **Manyetik silme (degaussing)** ve **fiziksel imha** ortamı kullanılamaz kılar ve elektronik atığa katkıda bulunur.
- **Katı hal sürücüleri ve flaş ortamlar**, silmenin kaçırdığı artık veriyi barındırabilir. Madde, yerleşik temizleme (sanitize) komutlarının doğru uygulandığında işe yaradığını, yazılım tekniklerinin ise çoğu zaman ama her zaman değil işe yaradığını bulan 2011 tarihli bir çalışmaya atıf yapar.
- **Şifreleme** başka bir yol sunar: kendi kendini şifreleyen bir sürücünün anahtarlarını yok etmek verisini erişilemez kılar.
- **Doğrulama ve sertifikalar:** iyi bir yazılım, üzerine yazmanın gizli alanlar dahil tüm cihaza ulaştığını doğrulamalı ve bir doğrulama sertifikası ile üzerine yazılamayan sektörlerin bir günlüğünü vermelidir.
- **Standartlar:** madde birçoğunu sıralar; bunların arasında, ikili sıfırlar gibi sabit bir örüntüyle tek bir üzerine yazma geçişinin tipik olarak kurtarmayı engellediğini söylediği alıntılanan NIST Special Publication 800-88 (2006, 2014'te gözden geçirildi) vardır. Modern sabit diskler için tek geçişin genellikle yeterli olduğunu belirtir.

Maddede alıntı gerektiği etiketi vardır ve bazı iddialar işaretlenmiştir. Sektörünüzün veya ülkenizin gerektirdiği standartlara ve ekipmanınız için güncel teknolojik duruma bakın; bir uyum kararı için Wikipedia özetine güvenmeyin.

### Elektronik atık

Wikipedia'daki elektronik atık maddesi onu, yeniden kullanım, yeniden satış, kurtarma, geri dönüşüm veya elden çıkarma için ayrılan öğeler dahil atılmış elektrikli veya elektronik cihazlar olarak tanımlar. 2022'de dünya genelinde yaklaşık 62 milyon ton üretildiğini, bunun 2010'a göre yüzde 82 arttığını ve 2024 tarihli bir çalışmaya göre yalnızca yüzde 22,3'ünün resmi olarak toplanıp geri dönüştürüldüğünü bildirir; çelişen başka rakamlara da atıf yapar ve doğrulanmamış iddialar için bakım etiketleri taşır; bu nedenle sayıları alıntılamadan önce birincil kaynaklarla karşılaştırın. Kurşun, kadmiyum, cıva ve alev geciktiriciler gibi malzemelerden ve kayıt dışı işlemeden kaynaklanan tehlikeleri, Çin'deki Guiyu ve Gana'daki Agbogbloshie örnekleriyle anlatır. Mart 1989'da kabul edilen Basel Sözleşmesi'nin tehlikeli atıkların sınır ötesi hareketini düzenlediğini ve R2 ile E-Stewards gibi programlar kapsamındaki sertifikalı geri dönüşümcülerin elektronik cihazlarda saklanan tüm verileri yok etmesi gerektiğini belirtir. Yeniden kullanım cihaz ömrünü uzatır ve geri dönüşümü geciktirir.

Bir kuruluş için çıkarılacak dersler pratiktir: sertifikalı olan ve cihazların nereye gittiğini gösterebilen elden çıkarma ortakları seçin, güvenli olduğunda yeniden kullanımı tercih edin ve kayıt tutun. Elektronik atık yasaları ülkeye ve bölgeye göre değişir; hangilerinin geçerli olduğunu uyum işlevinize sorun.

### Donanım ve hizmet yönetimi

Donanım kayıtları hizmetlere bağlanır: bu anahtar şu hizmeti taşır, bu sunucu şu uygulamayı barındırır. Bu bağlantılar bir varlık kaydını olay müdahalesi, değişiklik planlama ve risk değerlendirmesi için bir araca dönüştürür (bkz. Konu 4.4 — Yapılandırma Yönetimi). Onlar olmadan arızalı bir cihaz bir kayıttır (ticket); onlarla birlikte bir etki bildirimidir.

### Çeviklik ve donanım

Çevik ekipler donanımı, ana olay olarak değil, etrafında tasarım yapılacak bir kısıt olarak ele alır. Bulut ve sanallaştırma fiziksel varlığı azaltır ama sıfıra indirmez. Mobil uygulamalar için test cihazları, derleme ajanları, laboratuvar ekipmanı ve uç (edge) cihazların hepsinin izlenmesi gerekir. Bunları sahipleri ve yaşam döngüleri olan varlıklar olarak ele alın ve bir dolapta unutmayın.

## İyi uygulamalar

1. **Önemli olan her cihazı etiketleyin ve kaydedin.** Tesliminde benzersiz bir varlık etiketi veya seri numarası kaydı atayın ve türü, sahibi, konumu ve durumu kaydedin. Bunu teslimattan sonraki ilk adım yapın.
2. **Cihazları insanlara ve hizmetlere bağlayın.** Her cihazın kimde olduğunu ve hangi hizmeti desteklediğini kaydedin; taşınma ve değişikliklerde güncelleyin. Ekipmanı geri almak ve erişimi kaldırmak için işten ayrılma sürecini kullanın.
3. **Mali veriyi varlıkla birlikte tutun.** Maliyeti, garantiyi, destek koşullarını ve amortismanı kaydedin. Onarım, destek ve değiştirmeyi karşılaştırmak için kullanın.
4. **Bilinmeyeni bulmak için keşfi kullanın.** Kaydı ağ ve uç nokta keşfiyle karşılaştırın ve bilinmeyen cihazları hemen inceleyin (bkz. Konu 4.1 — BT Varlık Yönetimi).
5. **Durumu ve destek durumunu izleyin.** Garanti bitiş tarihlerini, bellenim ve güvenlik desteği durumunu ve arıza geçmişini takip edin. Cihazlar bozulmadan veya desteğini kaybetmeden önce değiştirmeyi planlayın.
6. **Kanıta göre değiştirin.** Değiştirme kararını yalnızca yaşa göre değil, arıza ve destek verilerine, performansa ve güvenlik desteğine bakarak verin. Politikayı yılda bir kez gözden geçirin.
7. **Cihazları tutarlı biçimde hazırlayın.** Yeni cihazlar hazır, güvenlik denetimleri yerinde gelsin diye standart bir yapı (build) ve otomatik kayıt (enrolment) kullanın.
8. **Güvenli olduğunda yeniden konuşlandırın.** İhtiyaçları hâlâ karşılayan cihazları silin ve yeniden atayın, silmenin kaydını tutun. Kullanılmayan ekipman yığınlarından kaçının.
9. **Veriyi düzgün silin ve kanıt saklayın.** Cihaz türüne ve verinin hassasiyetine uygun bir yöntem kullanın, doğrulayın ve bir sertifika veya günlük saklayın. Flaş depolama için uygun olduğunda cihazın desteklediği temizleme komutlarını veya anahtar imhasını kullanın (bkz. yukarıdaki veri silme notları).
10. **Elden çıkarma ortaklarını dikkatle seçin.** Sertifikalı geri dönüşümcüleri tercih edin, cihazların ve malzemelerin nereye gittiğini sorun ve kayıt tutun. Sözleşmeye veri imha koşullarını ekleyin.
11. **Kayıp ve çalıntı cihazları planlayın.** Bildirmek için hızlı bir yol, mümkün olduğunda uzaktan kilitleme veya silme ve bir kaybın ne zaman güvenlik olayı sayılacağına dair bir kural bulundurun (bkz. Konu 3.2 — Olay Yönetimi).
12. **Düzenli gözden geçirin.** Ana cihaz sınıfları için kayıttan bir örneklemi yılda en az iki kez fiziksel gerçeklikle karşılaştırın ve herhangi bir boşluğun arkasındaki süreci düzeltin.

## Ekibinizle tartışılacak sorular

**Bugün sahip olduğumuz her cihazı sayarsak, kayıtla eşleşir miydik?**

Bir kat, bir ekip veya bir depo seçin ve kayıtla hızlı bir sayım yapın. Farklar dersin kendisidir. Hangi uyumsuzlukların en çok önem taşıdığını sorun: üzerinde veri olan cihazlar, yamasız cihazlar. Kolaylaştırıcı, insanların değişiklik anında kaydı güncellemesini neyin engellediğini sorabilir. Sıkılaştırılacak bir süreç seçin.

**Biri ayrıldığında dizüstü bilgisayarla ne yapıyoruz?**

Adımları gözden geçirin: kim topluyor, nereye gidiyor, kim siliyor, kim kaydı güncelliyor. Boşluklar çoğu zaman ekipler arasında ortaya çıkar. Son örneği isteyin ve izini sürün. Tek bir sahipte ve bir kontrol listesinde anlaşın.

**Ekipmanı ne zaman değiştireceğimize nasıl karar veriyoruz?**

Mevcut kuralı ve kaynağını isteyin. Çoğu zaman bu, birinin uzun zaman önce belirlediği sabit bir yaştır. Arıza, destek maliyeti ve güvenlik desteği konusunda elinizde hangi verinin olduğunu tartışın. Erken veya geç değiştirme maliyetiyle karşılaştırın. Hangi verinin toplanacağında anlaşın.

**Elden çıkardığımız bir cihazdaki verinin yok edildiğini nasıl kanıtlardık?**

Yakın tarihli bir elden çıkarmayı alın ve hangi kanıtın bulunduğunu sorun. Yanıt "geri dönüşümcü öyle dedi" ise sertifika veya günlüğün neleri içermesi gerektiğini tartışın. Katı hal depolama için hangi yöntemin kullanıldığını sorun. Asgari bir standartta ve kanıtta anlaşın.

**Cihazlarımızdan hangilerinin garantisi veya güvenlik desteği bitti ve neler bunlara bağlı?**

Desteğin sonuna yaklaşan cihazları listeleyin. Her birinin neyi desteklediğini sorun. Önemli hizmetlerin arkasındaki desteksiz cihazlar risktir. Değiştirmeyi etki sırasına göre planlayın ve telafi edici önlemlerin nerede gerektiğine karar verin.

**Kayıp veya çalıntı bir cihazı kim ele alıyor ve ne kadar hızlı?**

Bir kullanıcının kaybı nasıl bildirdiğini ve sonrasında ne olduğunu sorun. Uzaktan kilitleme veya silmenin mümkün olup olmadığını ve kimsenin denemiş olup olmadığını kontrol edin. Bir kaybın ne zaman güvenlik olayına dönüştüğünü tartışın. Kullanıcılar için net bir ilk adımda anlaşın.

## Uygulamada: çevik bir ITIL örneği

Bir il sağlık kurumu, hastaları evlerinde ziyaret eden toplum hemşirelerine yaklaşık 4.000 dizüstü bilgisayar ve tablet sağlıyor. Cihazlar sık sık kayboluyor veya hasar görüyor. Kurumun kayıtları 4.300 cihaz gösteriyor, ancak hizmet masası daha azını yönettiğine inanıyor. Bir güvenlik incelemesi, emekliye ayrılmış olarak listelenen bir dizi dizüstü bilgisayarın kullanımda görüldüğünü ve bir dolapta duran eski cihaz stokunda hâlâ hasta verisi bulunduğunu saptıyor.

Son kullanıcı hizmetleri başkanı küçük bir program başlatıyor. Her cihaza benzersiz bir etiket ve adı belli bir hemşireye ve bir ekibe bağlı bir kayıt veriliyor. Bir keşif aracı kaydı ağa bağlanan cihazlarla karşılaştırıyor ve eşleşmeyen cihazların aylık listesi ekip yöneticilerine gidiyor; yöneticilerin bunları açıklamak veya iade etmek için iki haftası var. Cihazlar şifreleme açık ve standart yazılımla otomatik olarak kaydediliyor; böylece kaybolan bir dizüstü bilgisayar çok az şey açığa çıkarıyor. İşten ayrılma kontrol listesi, yöneticinin onayladığı bir adım olarak cihaz iadesini ekliyor. Emekliye ayırma için kurum, sürücüleri silen, silinemeyenleri imha eden ve her parti için bir sertifika veren sertifikalı bir geri dönüşümcüyle sözleşme yapıyor. Dolap boşaltılıyor, içindekiler siliniyor ve kaydediliyor.

Altı ay içinde kayıt ile keşif küçük bir fark payıyla eşleşiyor ve kaybolan bir dizüstü bilgisayar çoğu durumda bir saat içinde uzaktan kilitleniyor. Bazı sorunlar sürüyor. Hemşireler yoğun vardiyalarda bazen cihazları paylaşıyor, bu yüzden sahip alanı yanlış oluyor; geri dönüşümcünün sertifikaları partileri listeliyor ama tek tek cihazları listelemiyor ve denetçi bunu soruyor. Son kullanıcı hizmetleri başkanı günlük çıkış kaydı olan bir paylaşımlı cihaz kaydı getiriyor ve geri dönüşümcüden sertifikalara seri numaralarını eklemesini istiyor. Ayrıca değiştirme politikasını, sabit bir yaş yerine ilk yılın arıza verilerini kullanarak gözden geçirmeye karar veriyor.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekiplerinde test cihazları, derleme sunucuları ve laboratuvar ekipmanı bulunur. Bunları kaydedin, sahiplerini belirleyin ve düzgün biçimde emekliye ayırın. Cihazlara ihtiyaç duyduğunuzda varlık yönetimine bildirin; böylece tedarik projelerle eşleşir.

### Hizmet ve operasyon ekipleri

Operasyon ve hizmet masası yaşam döngüsünün çoğunu yürütür: derleme, dağıtım, destek ve emekliye ayırma. Her adımda kayıtları güncel tutun, boşlukları yakalamak için keşfi kullanın ve elden çıkarma kanıtlarını saklayın. Durum ve arıza verilerini değiştirmeyi planlayanlarla paylaşın.

### Liderlik ve yönetişim

Liderler değiştirme bütçelerine ve risk iştahına karar verir. Desteği biten cihaz sayısını, kayıp cihazlar için süreci ve veri imhasının kanıtını isteyin. Kanıta dayalı yenilemeyi ve kayıtları doğru tutan etiketler ve kontrol listeleri gibi küçük denetimleri destekleyin.

### Müşteriler ve kullanıcılar

Kullanıcılar ekipmanı gün be gün elinde tutar. Ona iyi bakın, kayıp veya hasarı hızla bildirin ve ayrıldığınızda ekipmanı iade edin. Bir cihazı paylaşıyorsanız veya başka bir konuma geçiyorsanız masaya bildirin; böylece kayıtlar doğru olur.

## Yaygın başarısızlık biçimleri

- **Etiketsiz ekipman.** Cihazlar birbirinden ayırt edilemez. Bunun yerine tesliminde etiketleyin ve kaydedin.
- **Eskimiş kayıtlar.** Taşınmalar ve ayrılanlar yakalanmaz. Bunun yerine güncellemeleri işe girme, yer değiştirme ve işten ayrılma süreçleri gibi olaylara bağlayın.
- **Veri olmadan sabit yaşa göre yenileme.** Cihazlar çok erken ya da çok geç değiştirilir. Bunun yerine arıza, maliyet ve destek verilerini gözden geçirin.
- **Zayıf elden çıkarma.** Elden çıkarılan cihazlarda veri kalır. Bunun yerine ortama uygun bir yöntemle silin ve doğrulayın, kanıt saklayın ve sertifikalı bir ortak kullanın.
- **Flaş depolamayı göz ardı etmek.** Üzerine yazmanın işe yarayacağı varsayılır. Bunun yerine temizleme komutlarını veya anahtar imhasını kullanın ve doğrulayın.
- **Stok yığınları.** Kullanılmayan cihazlar birikir. Bunun yerine bir takvimle yeniden konuşlandırın veya emekliye ayırın.
- **Hizmetlerle bağlantı olmaması.** Arızalı bir cihaz yalnızca bir kayıttır. Bunun yerine her cihazın desteklediği hizmeti kaydedin.
- **Sertifikasız geri dönüşüm.** Ekipman kimsenin bilmediği bir yere gider. Bunun yerine sertifikalı ortaklar seçin ve malzemelerin nereye gittiğini sorun.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Envanter ve izleme | Cihazlar gayriresmî olarak bilinir | Bir kayıt ana cihazları kapsar | Her cihaz etiketlenir ve kaydedilir, keşifle uzlaştırılır | Doğruluk ve boşluklar ölçülür ve düzeltilir | Envanter sahip olunan, kiralanan ve ortak cihazları paylaşılan verilerle kapsar |
| Yaşam döngüsü ve yenileme | Değiştirme arıza üzerine olur | Bazı cihazlar bir yenileme planını izler | Yaşam döngüsü adımları ve bir yenileme politikası tanımlıdır | Arıza ve maliyet verileri değiştirme kararlarını yönlendirir | Yenileme kuruluş genelinde tedarikçiler ve finansla planlanır |
| Elden çıkarma ve veri koruma | Elden çıkarma plansızdır | Bazı cihazlar silinir | Standart bir silme yöntemi ve kanıtlı, sertifikalı elden çıkarma | Elden çıkarma kanıtları denetlenir ve boşluklar kapatılır | Elden çıkarma ortaklar ve yeniden kullanım programlarıyla eşgüdümlüdür |
| Hizmet ve finansla bağlantı | Cihazlar hizmetlere veya maliyetlere bağlı değildir | Bazı maliyet verileri tutulur | Cihazlar sahiplere, hizmetlere ve maliyetlere bağlıdır | Maliyet ve destek verileri gözden geçirilir ve bütçelerde kullanılır | Varlık verileri finans, güvenlik ve tedarikçilerle sürekli paylaşılır |

## Kontrol listesi

- [ ] İzlediğimiz her cihazın benzersiz bir etiketi veya seri numarası kaydı ve adı belli bir sahibi veya kullanıcısı var.
- [ ] Cihazlar desteklediği hizmete bağlı.
- [ ] Keşif, ana cihaz türleri için kayıtla en az aylık karşılaştırılıyor.
- [ ] Garanti ve destek bitiş tarihleri kaydediliyor ve gözden geçiriliyor.
- [ ] Değiştirme politikamız veriye dayalı ve yıllık gözden geçiriliyor.
- [ ] İşten ayrılma ve yer değiştirme süreçleri cihazları geri alıyor veya yeniden atıyor.
- [ ] Veri silme, ortama uygun bir yöntemi doğrulama ve kayıtla kullanıyor.
- [ ] Elden çıkarma ortakları sertifikalı ve cihaz veya parti başına kanıt sağlıyor.
- [ ] Kayıp ve çalıntı cihazlar hızla bildirilebiliyor ve mümkün olduğunda uzaktan kilitlenebiliyor veya silinebiliyor.
- [ ] Kaydın bir örneklemi yılda iki kez fiziksel gerçeklikle karşılaştırılıyor.

## Yapay zeka istemleri

**Amaç: fiziksel bir sayımı kayıtla uzlaştırmak.**

```text
I have a physical count of devices in [location or team] and the register entries for the same scope.

Physical count (tag or serial, type, who has it): [paste].
Register (tag or serial, type, owner, status): [paste]. 

Using only these lists, identify items present physically but missing from the register, items in the register but not found, and items where the owner or status differs. For each group, suggest a question to ask. Do not guess about items that cannot be matched. List what you are unsure of.
```

**Amaç: veriye dayalı bir değiştirme incelemesi hazırlamak.**

```text
Help me prepare a replacement review for [device class, e.g. "field laptops"].

Data we have (age, repairs, failures, support tickets, warranty end, security support end, cost): [paste a table of real data].
Current replacement rule and its source: [paste, or write "unknown"].
Budget limits: [describe, or write "unknown"].

Using only this data, describe patterns by age group (for example failure and repair counts), identify devices near end of support, and suggest questions about whether the current rule fits. Do not invent failure rates or costs. If the data are too thin, say what to collect. List what you are unsure of.
```

**Amaç: kanıt gereksinimleriyle bir cihaz elden çıkarma kontrol listesi yazmak.**

```text
Help me write a disposal checklist for [device type, e.g. "laptops and phones"].

Data sensitivity: [describe].
Storage types: [for example hard drives, SSDs, phones with encrypted storage].
Disposal partner and what they provide: [describe, or write "not yet chosen"].
Rules we must follow, with source text: [paste, or write "none known"].

Produce a checklist covering authorization, removal of accounts and licenses, data erasure or destruction method by storage type, verification, evidence kept (certificate content, serial numbers), disposal route, and register update. Mark steps that are assumptions. Do not state that any law or standard requires a method unless I pasted its text. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: kayıp cihaz müdahalesi planlamak.**

```text
Draft a short response procedure for a lost or stolen [device type].

What controls exist today (encryption, remote lock, remote wipe, location): [describe, or write "unknown"].
Data the device may hold: [describe].
Who is told today: [list].

Write steps for the user, the service desk, and security: how to report, what to do in the first hour, when to treat the loss as a security incident, and how to record it. Leave any notification duty as [CHECK WITH LEGAL] unless I give the source text. Ask clarifying questions first, and list what you are unsure of.
```

## Yapay zeka becerileri

- [configuration-management](../../../../skills/configuration-management/SKILL.md): cihazları desteklediği hizmetlere bağlamak için kullanın.
- [capacity-planning](../../../../skills/capacity-planning/SKILL.md): ne kadar ekipmana ne zaman ihtiyaç olduğunu planlamak için kullanın.
- [budget-forecasting](../../../../skills/budget-forecasting/SKILL.md): yenileme ve destek maliyetlerini tahmin etmek için kullanın.
- [data-governance](../../../../skills/data-governance/SKILL.md): cihazlardaki verinin sahibini ve emekliye ayırma sırasında nasıl korunacağını belirlemek için kullanın.
- [vendor-management](../../../../skills/vendor-management/SKILL.md): donanım tedarikçilerini ve elden çıkarma ortaklarını seçmek ve gözden geçirmek için kullanın.

## Temel kaynaklar

- **IT asset management** (Wikipedia): veri merkezi yönetimi maddesinin içinde tanım ve donanım varlık yönetiminin bir tanımı.
- **Data erasure** (Wikipedia): yöntemler, standartlar, doğrulama ve katı hal depolamanın özel durumu.
- **Electronic waste** (Wikipedia): ölçek, tehlikeler, geri dönüşüm ve Basel Sözleşmesi; çelişen rakamlara dair uyarılarla.
- **Guidelines for Media Sanitization** (NIST Special Publication 800-88): Wikipedia maddesinin alıntıladığı birincil rehberlik; bir standart belirlemeden önce güncel gözden geçirilmiş sürümü okuyun.

## Kaynakça

1. IT asset management — Wikipedia — https://en.wikipedia.org/wiki/IT_asset_management
2. Data erasure — Wikipedia — https://en.wikipedia.org/wiki/Data_erasure
3. Electronic waste — Wikipedia — https://en.wikipedia.org/wiki/Electronic_waste
4. Basel Convention — Wikipedia — https://en.wikipedia.org/wiki/Basel_Convention
5. Data center management — Wikipedia — https://en.wikipedia.org/wiki/Data_center_management
6. Total cost of ownership — Wikipedia — https://en.wikipedia.org/wiki/Total_cost_of_ownership
7. Mobile device management — Wikipedia — https://en.wikipedia.org/wiki/Mobile_device_management
8. Information security — Wikipedia — https://en.wikipedia.org/wiki/Information_security
