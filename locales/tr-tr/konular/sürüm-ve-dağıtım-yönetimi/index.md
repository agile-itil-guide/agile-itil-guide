# Sürüm ve Dağıtım Yönetimi

**Sürüm ve dağıtım yönetimi, değişiklikleri güvenle üretime ulaştırır; çevik bir ortamda amaç, sürüm yayımlamayı o kadar rutin, otomatik ve geri alınabilir kılmaktır ki bir olay olmaktan çıksın.**

## Bu neden önemli

Birçok kuruluş bir sürümü hâlâ büyük, gergin bir olay olarak görür. Bir tarih belirlenir, bir pencere ayrılır, insanlar geç saatlere kadar kalır ve başarı, bir şeyin bozulup bozulmadığıyla ölçülür. Bu örüntü, korktuğu riski tam olarak üretir: bir sürümde ne kadar çok değişiklik toplulaştırılırsa, neyin yanlış gittiğini anlamak o kadar zorlaşır ve geri alma o kadar acı verici olur.

DORA'nın araştırma programı alternatifi anlatır. Sürekli teslimat hakkındaki sayfası uygulamayı "her türlü değişikliği isteğe bağlı olarak hızla, güvenle ve sürdürülebilir biçimde yayımlama yeteneği" olarak tanımlar ve bunu iyi yapmanın teslimat performansını ve erişilebilirliği iyileştirdiğini, daha düşük tükenmişlik ve daha yüksek iş memnuniyetiyle ilişkili olduğunu bildirir. Sayfası ayrıca süreçleri ve mimariyi değiştirmeden daha sık dağıtım yapmanın başarısızlık oranlarını yükseltme ve ekipleri tüketme eğiliminde olduğu konusunda uyarır. Ders "daha hızlı yayımla" değil, "güvenle yayımlama yeteneğini oluştur, sonra sık yayımla"dır.

Google'ın *Site Reliability Engineering* kitabı, sürüm mühendisliği bölümünde uygulamadan benzer bir noktaya değinir: sık sürümler, sürümler arasında daha az değişiklik demektir; bu nedenle sınama ve sorun giderme kolaylaşır. Bu konu bu iki kaynaktan, kılavuzun değişiklikle ilgili diğer konularından ve bu kılavuzun çerçeve sahibinin metnine karşı doğrulayamadığı, yaygın kullanılan ITIL sözcük dağarcığından yararlanır. Kaynakları güçlü, belirli ve anlattıkları bağlamlarla sınırlı olarak görün.

## Temel kavramlar

### Sürüm ve dağıtım

İki terim sıklıkla karıştırılır. Hizmet yönetiminde yaygın kullanılan bir ayrım şudur:

- **Sürüm** (release), bir hizmetin veya bileşenin kullanıma sunulan bir versiyonudur. Kullanıcıların ne alacağına dair bir karardır.
- **Dağıtım** (deployment), bir versiyonu üretim gibi bir ortama taşıma eylemidir.

Bunları ayırmak güçlüdür. Kodu kullanıcılar için açmadan üretime dağıtabilir ve sonra denetimli biçimde yayımlayabilirsiniz. Özellik anahtarları gibi teknikler bu ayrıma dayanır (bkz. Wikipedia'nın özellik anahtarları maddesi).

### Sürekli teslimat ve sürekli dağıtım

DORA'nın sayfası **sürekli teslimatı** (continuous delivery), her türlü değişikliği isteğe bağlı olarak hızla, güvenle ve sürdürülebilir biçimde yayımlama yeteneği olarak tanımlar. Bunu, her değişikliği olabildiğince çabuk üretime dağıtmak anlamına gelen **sürekli dağıtımdan** (continuous deployment) ayırır. DORA, ekiplerin sürekli dağıtımı hiç benimsemeseler bile "sürekli teslimatla başlayabileceğini ve başlaması gerektiğini" söyler. Yayımlayıp yayımlamama kararı bir iş kararı olarak kalır; sürekli teslimat onu bir proje değil, bir seçim yapar.

### Araştırmanın önerdiği şeyler

DORA sayfası sürekli teslimatı destekleyen uygulamaları listeler:

| Uygulama | DORA ne söyler |
|---|---|
| **Test otomasyonu** | Çoğunlukla geliştiriciler tarafından oluşturulan ve sürdürülen kapsamlı, güvenilir otomatik test kümeleri |
| **Dağıtım otomasyonu** | Elle müdahale gerektirmeyen, tamamen otomatik dağıtımlar |
| **Gövde tabanlı geliştirme** (trunk-based development) | Üçten az etkin dal, çok kısa ömürlü dallar, nadir kod kilidi dönemleri |
| **Gevşek bağlı ekipler ve mimari** | Ekiplerin diğer hizmetlerle eşgüdüm gerektirmeden isteğe bağlı sınama ve dağıtım yapabilmesi |
| **Diğer uygulamalar** | Sürekli tümleştirme, sürekli sınama, tüm üretim yapıtları için sürüm denetimi, test verisi yönetimi, izleme ve gözlemlenebilirlik, proaktif bildirimler, veritabanı değişiklik yönetimi, yaygın güvenlik |

Sayfa, sürekli teslimatın daha yüksek kaliteyle (yeniden işe veya planlanmamış işe harcanan daha az zaman), daha düşük tükenmişlikle ve daha az dağıtım acısıyla ilişkili olduğunu bildirir. Ayrıca 2021 raporunda güvenilirlik hedeflerini karşılayan elit ekiplerin, düşük performans gösterenlere kıyasla gevşek bağlı bir mimariye sahip olma olasılığının üç kat daha fazla olduğunu söyler. Hiçbir araç, hedef dağıtım sıklığı veya uygulama takvimi belirtmez ve dönüşümlerin otomasyon test gereksinimlerini artırdıkça ve teknik borç biriktikçe verimlilikte bir düşüşle yaygın olarak bir "J eğrisi"ni izlediğini not eder.

### Sürüm mühendisliği uygulamasından dersler

SRE kitabının sürüm mühendisliği bölümü, büyük bir kuruluşun yaklaşımını anlatır:

- **Self servis.** Ekipler kendi sürüm süreçlerini yürütür. Sürümler "gerçekten otomatiktir" ve mühendis katılımını yalnızca sorun çıkarsa gerektirir.
- **Yüksek hız.** Sık sürümler, versiyonlar arasında daha az değişiklik demektir; bu da sınama ve sorun gidermeyi kolaylaştırır.
- **Hermetik derlemeler.** Derlemeler bilinen araç ve kütüphane versiyonlarına dayanır; böylece aynı revizyon aynı sonuçları verir.
- **Uygulanan politikalar.** Erişim denetimleri onayları, sürüm oluşturmayı ve dağıtımı kapılar. Neredeyse tüm değişiklikler kod gözden geçirmesi gerektirir ve her sürüm, içerdiği değişikliklerin bir raporunu üretir.

Bölüm ayrıca kaynak denetimi ve kod gözden geçirmesi altında yapılandırmayı vurgular ve geliştiricilerin, site güvenilirliği mühendislerinin ve sürüm mühendislerinin sonuçları "çitin üzerinden atmak" yerine iş birliği yapmasını önerir. Kuruluşların henüz otomatikleştiremeseler veya uygulatamasalar bile sürüm politikaları tanımlaması gerektiğini ve iyi uygulamaları erken yerleştirmenin sonradan uyarlamaktan daha ucuz olduğunu söyler. Bölüm Google'ın kendi araçlarını anlatır; ortamınız farklı olanları kullanacaktır; bu nedenle ürünleri değil, ilkeleri alın.

### Ortamlar ve terfi

Bir sürüm genellikle geliştirme, test ve üretim gibi bir dizi ortamdan geçer. Her adım kanıt sağlar. Yukarıdaki araştırmayla tutarlı yaygın bir uygulama, bir kez derleyip aynı yapıtı terfi ettirmektir; böylece sınanan, dağıtılanla aynı olur. SRE bölümünün aynı revizyondan özdeş derlemelere vurgusu aynı fikri ifade eder.

### Kullanıma alma ve geri alma

Bir sürümün kullanıcılara ulaşma biçimi kademeli olabilir. SRE bölümü, geliştirmede saatlik otomatik itmelerden hassas altyapı için çok günlük kullanıma almalara kadar riske göre tempolanan kullanıma almaları anlatır ve trafiğin küçük bir payının yeni versiyonu önce aldığı kanarya sürümlerinden söz eder. Geri alma önceki versiyona dönmek demektir ve kullanıma alma kadar pratik edilmiş olmalıdır. Hızla geri dönebilen ekipler sık dağıtım yapmayı göze alabilir (bkz. Konu 3.4 — Değişiklik Sağlama).

### Destek için sürüm bilgisi

Destek personelinin ve kullanıcıların neyin değiştiğini ve bir şey ters giderse ne yapılacağını bilmesi gerekir. Bir sürüm notu, bilinen sorunlar listesi ve adlandırılmış bir iletişim kişisi asgari düzeydir (bkz. Konu 3.1 — Hizmet Masası). SRE bölümünün dâhil edilen değişikliklerin sürüm raporu bir kaynak olarak hizmet eder.

### Ölçümler

DORA'nın sayfası, düzenli ve acil değişiklikler için kısa teslim sürelerini, düşük değişiklik başarısızlık oranlarını, kısa hizmeti geri getirme süresini ve öncelikleri zamanında teslim eden sürüm sıklıklarını ölçmeyi önerir. Her şeyi kapsayan hedefi, kimsenin dağıtım için mesai saatleri dışında çalışmamasıdır. Ölçümlerin tanımları ve uyarıları için bkz. Konu 3.4 — Değişiklik Sağlama ve Konu 5.6 — Metrikler ve Ölçüm.

## İyi uygulamalar

1. **Dağıtımı sürümden ayırın.** Kodu üretime uykuda bir durumda dağıtın ve hazır olduğunda özellik anahtarları veya aşamalı kullanıma almalarla kullanıcılar için açın. Bu, bir dağıtımın riskini azaltır ve işe denetim verir.
2. **Dağıtımı otomatikleştirin.** Elle adım olmamasını hedefleyin. Elle adımlar yavaştır, kişiler arasında değişir ve olaylara neden olur. Küçük artışlarla, en çok ters giden adımlardan başlayarak otomatikleştirin.
3. **Bir kez derleyin, yapıtı terfi ettirin.** Tek bir paket üretin ve ortamlar boyunca taşıyın; böylece sınadığınız şey çalıştırdığınız şey olur. Hangi versiyonun nerede olduğunu kaydedin.
4. **Derlemeleri yeniden üretilebilir yapın.** Araç ve kütüphane versiyonlarını sabitleyin; böylece aynı revizyon aynı sonucu verir. Bu, SRE bölümünün hermetik derleme ilkesini izler.
5. **Dalları kısa ömürlü tutun.** DORA'nın gövde tabanlı rehberliği, üçten az etkin dal ve yaklaşık bir gün içinde birleşen dallardır. Uzun dallar sürümleri birleştirme olaylarına dönüştürür.
6. **Otomatik sınayın ve testleri hızlı ve güvenilir tutun.** Dakikalar içinde geri bildirimi hedefleyin. Kararsız veya yavaş bir test kümesi insanların onu atlamasına yol açar.
7. **Küçük partiler hâlinde yayımlayın.** Daha küçük sürümlerin gözden geçirilmesi, sınanması ve geri alınması daha kolaydır. Bir sürüm büyükse nasıl bölüneceğini sorun.
8. **Aşamalı olarak kullanıma alın.** Kullanıcıların veya sunucuların küçük bir payıyla başlayın, sinyalleri izleyin ve genişletin. Neyi izleyeceğinizi ve kimin kullanıma almayı durdurabileceğini önceden tanımlayın.
9. **Geri almayı prova edin.** Son iyi versiyona nasıl dönüleceğini bilin ve pratik yapın. Hiç denemediğiniz bir geri alma bir umuttur.
10. **Destek ekibine sürümden önce ihtiyaç duyduklarını verin.** Sürüm notlarını, bilinen sorunları ve bir iletişim kişisini sağlayın. Kullanıcıları etkileyen değişikliklerin onayına destek personelini dâhil edin (bkz. Konu 3.1 — Hizmet Masası).
11. **Yapılandırmayı sürüm denetiminde tutun.** Yapılandırma değişikliklerini kod gibi, gözden geçirme ve kayıtla ele alın. Her tür ayarın nerede yaşadığını ve nedenini seçin.
12. **Mesai saatlerinde dağıtımı hedefleyin.** DORA bunu her şeyi kapsayan hedef olarak adlandırır. Dağıtımlar geç saatlere kadar sürüyorsa süreç veya mimari üzerinde çalışılması gerekir.

## Ekibinizle tartışılacak sorular

**Bitmiş bir değişikliği üretime almak ne kadar sürüyor ve kaç adım içeriyor?**

Yakın zamandan bir değişikliği "hazır"dan "canlı"ya kadar izleyin. Her adımı, kimin yaptığını ve ne kadar beklediğini listeleyin. Elle adımları otomatik olanlardan ayırın. Ekipler çoğu zaman kaç adımın elle olduğuna ve aralarındaki beklemeye şaşırır. Kolaylaştırıcı, hangi adımın en çok olaya neden olduğunu sorabilir. Otomatikleştirilecek bir tane seçin.

**Endişelenmeden mesai saatlerinde sürüm yayımlayabilmemiz için neyin doğru olması gerekir?**

Ekibin sürüm yayımlamaktan neden korktuğunu sorun. Tipik yanıtlar: sınanmış bir geri alma yok, zayıf testler, kullanıcılara etkisi belirsiz. Her biri inşa edilecek bir şeydir. Bunları listeleyin ve sıralayın. İlki için en küçük adımın ne olacağını sorun. DORA'nın kimsenin dağıtım için mesai saatleri dışında çalışmaması hedefi tartışmak için yararlı bir hedeftir.

**Sürüm yayımlamak acı verici olduğu için değişiklikleri nerede toplulaştırıyoruz ve bu bize neye mal oluyor?**

Yakın zamandaki sürümlerin içeriğine bakın. Her birindeki değişiklikleri sayın. Bir topluluk ters gittiğinde ne olduğunu ve nedeni bulmanın ne kadar sürdüğünü sorun. Tek değişiklikli sürümleri neyin kolay yol yapacağını tartışın. Düşük riskli bir değişikliği tek başına yayımlamak gibi ilk bir adım üzerinde anlaşın.

**Bir sürüm canlıya çıktıktan sonra çalıştığını nasıl biliyoruz?**

Ekibin ilk saatte hangi sinyallere baktığını sorun: hatalar, performans, kullanıcı bildirimleri. Yanıt "şikâyetleri bekliyoruz" ise, bir sorunu çabucak gösterecek izlemeyi tartışın. Kimin izlediğini ve ne yapacağını sorun. Sürüm sonrası için kısa bir kontrol listesi üzerinde anlaşın.

**Destek ekibimiz bir sürüm çıkmadan önce hakkında ne biliyor?**

Hizmet masasına son sürüm hakkında ne öğrendiklerini ve ne zaman öğrendiklerini sorun. İhtiyaç duyduklarıyla karşılaştırın. Bir sürüm notu ve adlandırılmış bir iletişim kişisi gibi basit bir devir teslimi tartışın. Riskli sürümlerin planlamasına kullanıcıların sorularını yanıtlayan kişileri dâhil edin.

**Bir dondurma dönemi olmadan dağıtım yapmamızı ne engelliyor ve bir dondurma dönemi bize neye mal olur?**

Dondurma dönemleri, zirve iş zamanları etrafında yaygındır. Ne kadar sürdüklerini ve neyi geciktirdiklerini sorun. Küçük, iyi sınanmış değişikliklerin ek güvencelerle bu dönemlerde ilerleyip ilerleyemeyeceğini tartışın. DORA sayfası, risk veya zamanlamaya bakılmaksızın tüm değişikliklere aynı onayı uygulamaya karşı uyarır; bu nedenle dondurmanın fazla kaba olup olmadığını sorun.

## Uygulamada: çevik bir ITIL örneği

Bir üniversite, 30.000 öğrenci için bir çevrimiçi kayıt sistemi işletir. Sekiz kişilik geliştirme ekibi dönemde bir kez, kayıtlar açılmadan önce bir hafta sonu penceresinde sürüm yayımlar. Her sürüm yüzlerce değişikliği toplulaştırır ve on beş kişi, uzun bir elle kontrol listesi ve bir çağrı planı gerektirir. Son sürüm Pazar sabahı saat 2'de başarısız oldu ve ekip hangi değişikliğin buna neden olduğunu bulmak için on dört saat harcadı.

Ekip lideri bir yaklaşım değişikliği önerir. Birincisi, dağıtımlar tamamen betiklenir; son seferde başarısız olan adımlardan başlanır. İkincisi, ekip kayıt yolu için her değişiklikte çalışan ve on dakikadan kısa süren otomatik testler ekler. Üçüncüsü, yeni özellikler kapalı olarak dağıtılır ve kontrollerden sonra bir özellik anahtarıyla etkinleştirilir. Dördüncüsü, bir geri alma adımı yazılır ve bir test ortamında prova edilir. Öğrenci işleri dairesi, kullanıcıya görünür bir arıza düzeltmesi olmadıkça, yoğun kayıtların üç haftası boyunca hiçbir sürümün üretime çıkmayacağı bir kural üzerinde anlaşır.

Bir dönem içinde ekip, yoğun olmayan haftalarda, mesai saatlerinde, sürüm notları bir gün önce öğrenci yardım masasına gönderilerek haftalık dağıtım yapar. Bazı sürümler kararsız testlerle yavaşlar ve bir özellik anahtarı yanlışlıkla açık bırakılıp kısa bir karışıklığa neden olur. Dönüşüm ayrıca DORA sayfasının anlattığı J eğrisine de çarpar: iki ay boyunca testler ve betikler üzerindeki çalışma özellik teslimatını yavaşlatır. Ekip devam eder, kararsız testleri düzeltir, anahtarları kaldırmak için bir kontrol listesi adımı ekler ve dondurma kuralını gelecek yıl gözden geçirmek üzere öğrenci işleriyle anlaşır. Dönemin kayıt zirveleri sürümle ilgili bir olay olmadan geçer.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

İşlem hattı teslimat ekiplerine aittir: testler, derlemeler, dağıtım betikleri ve geri alma. Onlara kullanıcıları olan bir ürün gibi yatırım yapın. Küçük yayımlayın, sık yayımlayın ve her sürümü işlem hattı hakkında kanıt olarak görün. Değişiklikler onları etkilediğinde destek ve operasyonu dâhil edin.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri daha küçük, daha öngörülebilir sürümlerden yararlanır ve bir sürümün kabulünden önce neyin doğru olması gerektiğini tanımlayarak yardımcı olabilir: izleme, çalışma kılavuzları ve geri alma. Kapı bekçiliğinden, teslimat ekiplerinin kullandığı platformu ve kontrolleri sağlayarak olanak sağlamaya geçin. Sürümden sonra sinyalleri izleyin.

### Liderlik ve yönetişim

Ekiplerin işlem hattına yatırım yapıp yapamayacağına ve J eğrisine tahammül edip edemeyeceğine liderler karar verir. Teslim süresini, değişiklik başarısızlık oranını ve toparlanma süresini isteyin. Sürümleri riske genel bir yanıt olarak dondurmaya direnin ve bunun yerine riskli sürümlerin daha fazla inceleme gördüğüne dair kanıt isteyin.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar sık küçük iyileştirmeler ve daha az büyük patlamalı kesinti görür. Sizi etkileyen değişikliklerin önceden bildirilmesini ve sorunları bildirmek için bir yol bekleyin. Yoğun dönemleriniz varsa, aşamalı kullanıma almaları bunların etrafında planlayabilsinler diye sağlayıcıya söyleyin.

## Yaygın başarısızlık biçimleri

- **Büyük patlamalı sürümler.** Yüzlerce değişiklik birlikte çıkar. Bunun yerine küçük partiler hâlinde yayımlayın ve dağıtımı sürümden ayırın.
- **Elle dağıtım.** Adımlar kişiye göre değişir ve geceleri başarısız olur. Bunun yerine en riskli adımlardan başlayarak artımlı biçimde otomatikleştirin.
- **Güvencesiz daha sık sürüm yayımlamak.** DORA'nın uyardığı gibi başarısızlık oranları artar ve insanlar tükenir. Bunun yerine önce testlere, geri almaya ve izlemeye yatırım yapın.
- **Farklı ortamlarda farklı yapıtlar.** Sınanan, çalışan değildir. Bunun yerine bir kez derleyin ve aynı yapıtı terfi ettirin.
- **Uzun ömürlü dallar.** Birleştirmeler birer olay olur. Bunun yerine dalları kısa tutun ve sürekli tümleştirin.
- **Denenmemiş geri alma.** İlk geri alma bir kesinti sırasında gerçekleşir. Bunun yerine düzenli olarak prova edin.
- **Destek en son bilir.** Personel değişiklikleri kullanıcılardan öğrenir. Bunun yerine sürümden önce sürüm notları ve bir iletişim kişisi gönderin.
- **Toptan dondurmalar.** Aynı dondurma tüm değişikliklere uygulanır. Bunun yerine düşük riskli, iyi sınanmış değişikliklerin ek kontrollerle geçmesine izin verin ve dondurmayı riskli olan için saklayın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Dağıtım otomasyonu | Dağıtımlar elle yapılır ve değişir | Bazı dağıtımlar betiklenmiştir | Dağıtımlar ortak bir işlem hattıyla otomatiktir | Dağıtım başarısızlıkları ve süresi izlenir ve azaltılır | İşlem hatları ve uygulamalar ekipler arasında paylaşılır ve iyileştirilir |
| Sürüm sıklığı ve boyutu | Sürümler nadir ve büyüktür | Bazı ekipler daha küçük partiler hâlinde yayımlar | Ekipler bilinen bir ritimle küçük partiler hâlinde yayımlar | Sıklık, teslim süresi ve boyut ölçülür ve ayarlanır | Sürüm ritimleri hizmetler ve tedarikçiler arasında eşgüdümlenir |
| Güvenlik (testler, kullanıma alma, geri alma) | Sınama elle yapılır; geri alma denenmemiştir | Bazı otomatik testler ve geri alma adımları vardır | Otomatik testler, aşamalı kullanıma alma ve prova edilmiş geri alma standarttır | Değişiklik başarısızlık oranı ve toparlanma süresi izlenir ve iyileştirilir | Güvenlik uygulamaları ekipler arasında paylaşılır ve sınanır |
| Destek hazırlığı | Destek sürümleri kullanıcılardan öğrenir | Bazı sürümlerin notları vardır | Sürüm notları ve iletişim kişileri standarttır | Sürümler hakkındaki destek geri bildirimi toplanır ve ona göre hareket edilir | Destek, teslimat ve kullanıcılar sürümleri birlikte planlar |

## Kontrol listesi

- [ ] Dağıtmak ile yayımlamak arasındaki farkı söyleyebiliyoruz ve bunu kullanıyoruz.
- [ ] Dağıtımlar elle adım olmadan otomatiktir ya da kalan elle adımlar listelenmiştir.
- [ ] Bir kez derliyor ve aynı yapıtı ortamlar boyunca terfi ettiriyoruz.
- [ ] Otomatik testler her değişiklikte çalışıyor ve dakikalar içinde geri bildirim veriyor.
- [ ] Dallar kısa ömürlüdür ve sık sık gövdeye birleştirilir.
- [ ] Her sürüm türü için bir geri alma vardır ve prova edilmiştir.
- [ ] Kullanıma almalar, risk gerektirdiğinde sinyaller önceden tanımlanarak aşamalıdır.
- [ ] Sürüm notları ve bilinen sorunlar bir sürümden önce hizmet masasına ulaşıyor.
- [ ] Yapılandırma sürüm denetimindedir ve gözden geçirilir.
- [ ] Her hizmet için teslim süresini, değişiklik başarısızlık oranını ve toparlanma süresini izliyoruz.

## Yapay zeka istemleri

**Amaç: "hazır"dan "canlı"ya adımları haritalamak ve neyin otomatikleştirileceğini bulmak.**

```text
Help me map the path of a change from ready to live.

The steps in order, with who does each, whether it is manual or automated, and how long it typically waits or takes: [paste].
The last three releases and what went wrong, if anything: [paste facts].

Produce a table of steps and mark the manual ones. Rank the manual steps by how often they caused problems in the text, and suggest, for the top three, one small way to automate or check each. Do not invent durations or failure counts. Ask clarifying questions first if information is missing, mark assumptions, and list what you are unsure of.
```

**Amaç: hizmet masası ve kullanıcılar için bir sürüm notu yazmak.**

```text
Write a release note for [service].

What changed (plain words): [describe].
Who is affected and when: [describe].
What users will notice: [describe].
Known issues and workarounds: [list, or write "none known"].
How to roll back and who to contact: [describe].

Write two versions: a one-paragraph note for users and a half-page note for the service desk. Use only the facts above. Mark any statement that is an assumption and ask clarifying questions first if information is missing. List what you are unsure of.
```

**Amaç: aşamalı bir kullanıma almayı planlamak.**

```text
Plan a staged rollout of [change].

What it changes and who uses it: [describe].
How we can limit exposure (percentage of users, regions, servers, feature switch): [describe options available].
Signals we can watch: [list monitoring and user feedback sources].
Rollback method: [describe].

Propose stages, what to check at each stage, who can pause or stop, and what would trigger a rollback, leaving numeric thresholds as [to be agreed]. Do not invent monitoring that we do not have. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Amaç: sürüm otomasyonuna yatırım yapmak için bir gerekçe hazırlamak.**

```text
Help me prepare a short case for investing in release automation for [service].

What a release costs us today, in facts: [people involved, hours, incidents, delays; use real numbers only].
What we want to be able to do: [describe].
Known risks of the work: [for example a temporary slowdown while tests are written].

Write a one-page case with the problem, the proposed first steps (small and incremental), what we will measure (lead time, change fail rate, recovery time, with no targets that I did not give), the risks including a temporary dip in delivery, and what we ask for. Do not invent figures. Ask clarifying questions first, and list what you are unsure of.
```

## Yapay zeka becerileri

- [release-notes](../../../../skills/release-notes/SKILL.md): kullanıcılara ve hizmet masasına bir sürümün neyi değiştirdiğini anlatmak için kullanın.
- [changelog](../../../../skills/changelog/SKILL.md): değişikliklerin versiyona göre sürekli bir kaydını tutmak için kullanın.
- [test-driven-development](../../../../skills/test-driven-development/SKILL.md): sık sürüm yayımlamayı güvenli kılan otomatik testleri oluşturmak için kullanın.
- [shift-left-testing](../../../../skills/shift-left-testing/SKILL.md): sorunların daha erken bulunması için sınamayı işlem hattında öne almak için kullanın.
- [agile-delivery](../../../../skills/agile-delivery/SKILL.md): küçük, sık sürümleri ve etraflarındaki kontrolleri planlamak için kullanın.

## Temel kaynaklar

- **Continuous delivery** (DORA, dora.dev): araştırma programının tanımı, önerilen uygulamaları, bulguları ve tuzakları.
- **Release Engineering** (*Site Reliability Engineering*, Google, sre.google): bir kuruluşun self servis, yeniden üretilebilir derlemeler ve uygulanan sürüm politikası uygulaması.
- **Streamlining change approval** (DORA, dora.dev): onayın teslimata nasıl uyduğuna dair rehberlik.
- **Continuous delivery** (Wikipedia): uygulamaya ve tarihine genel bakış.

## Kaynakça

1. Continuous delivery — DORA, dora.dev — https://dora.dev/capabilities/continuous-delivery/
2. Release Engineering — Google SRE book, sre.google — https://sre.google/sre-book/release-engineering/
3. Streamlining change approval — DORA, dora.dev — https://dora.dev/capabilities/streamlining-change-approval/
4. Continuous delivery — Wikipedia — https://en.wikipedia.org/wiki/Continuous_delivery
5. Software deployment — Wikipedia — https://en.wikipedia.org/wiki/Software_deployment
6. Release management — Wikipedia — https://en.wikipedia.org/wiki/Release_management
7. Feature toggle — Wikipedia — https://en.wikipedia.org/wiki/Feature_toggle
8. Continuous integration — Wikipedia — https://en.wikipedia.org/wiki/Continuous_integration
9. Version control — Wikipedia — https://en.wikipedia.org/wiki/Version_control
