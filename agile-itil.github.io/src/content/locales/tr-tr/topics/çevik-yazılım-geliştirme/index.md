# Çevik Yazılım Geliştirme

**Çevik yazılım geliştirme, yazılımı küçük adımlarla teslim eden ve geri bildirimden öğrenen sürekli yazılım teslimi yöntemleri ailesidir; otomatik test ve sürekli entegrasyon gibi ürettiği uygulamalar, değişen hizmetleri güvenle işletmenin pratik temelidir.**

## Bu neden önemli

Bir BT hizmeti işleten ekiplerin çoğu onu aynı zamanda geliştirir ve değiştirir. Yazılımın nasıl geliştirildiği, hizmetin ne sıklıkla değiştiğini, her değişikliğin ne kadar riskli olduğunu ve nöbetçi kişilerin kendilerine verilene ne kadar güvenebileceğini belirler. Büyük yığınlar halinde geliştiren ve nadiren devir teslim yapan bir ekip, operasyona birkaç büyük ve korkutucu sürüm verir. Küçük adımlarla, testler ve hızlı geri bildirimle geliştiren bir ekip ise onlara birçok küçük ve anlaşılır sürüm verebilir.

Çevik yazılım geliştirme, ikinci çalışma biçiminin en bilinen fikirler bütünüdür. Aynı zamanda yaygın biçimde yanlış anlaşılır. Bazıları "çevik" sözcüğünü "plan yok, belge yok" anlamında, bazıları ise günlük toplantısı olan her süreç için kullanır. Bu konu daha net bir resim verir: çevik yöntemlerin nereden geldiği, ortak noktalarının ne olduğu, neyi iddia etmedikleri ve bir hizmeti ayakta tutmak zorunda olan bir ekip için hangi uygulamaların en önemli olduğu.

Kanıt dikkatli bir okuma gerektirir. [Çevik yazılım geliştirme hakkındaki Wikipedia maddesi](https://en.wikipedia.org/wiki/Agile_software_development), çeviklik için anekdotal kanıtın güçlü olduğunu ama ampirik kanıtın "sınırlı ve kesin sonuç vermeyen" nitelikte olduğunu söyler ve yıllık State of Agile anketi gibi, yararları bildiren ama kendi bildirimli görüşlere dayanan anketlere işaret eder. Çevik yöntemleri kendi ortamınızda sınanacak umut verici yaklaşımlar olarak ele alın.

## Temel kavramlar

### Terim neyi kapsıyor

"Çevik yazılım geliştirme" bir şemsiye terimdir. Wikipedia maddesi onu, 2001'de 17 uygulayıcının üzerinde anlaştığı değerlerden ve ilkelerden büyüyen yaklaşımları kapsayan bir terim olarak tanımlar (bkz. Konu 1.1 — Çevik Manifesto ve Konu 1.2 — Çevik İlkeler). Büyük harfle "Agile" çoğunlukla o zihniyetten doğan uygulamalar için, küçük harfle "agile" ise uyum sağlayabilme niteliği için kullanılır. Ayrım katı değildir ve ikisini de duyarsınız.

Çevik yöntemler sürekli yazılım teslimini amaçlar. Paydaşlar ile geliştiriciler arasındaki sürekli iş birliğine dayanır, projeleri motivasyonu yüksek bireyler etrafında kurar ve kaliteye özen göstererek geri bildirim yoluyla sürekli iyileştirmeyi izler. Neyi vurguladıklarında ayrılırlar. Extreme Programming gibi bazıları mühendislik uygulamalarına, Scrum ve Kanban gibi diğerleri ise işin nasıl yönetildiğine odaklanır.

### Kısa bir tarihçe

Wikipedia maddesi, yinelemeli ve artımlı geliştirmenin izini 1957'ye kadar sürer; evrimsel proje yönetimi ve uyarlanabilir yazılım geliştirme 1970'lerin başında ortaya çıkar. 1990'larda, çoğunlukla [şelale modeli](https://en.wikipedia.org/wiki/Waterfall_model) denen ağır, plan güdümlü süreçlere tepki olarak bir hafif yöntemler grubu ortaya çıktı. Madde hızlı uygulama geliştirmeyi (1991), birleşik süreci ve dinamik sistem geliştirme yöntemi DSDM'yi (1994), Scrum'ı (1995), Crystal Clear ve Extreme Programming'i (1996) ve özellik güdümlü geliştirmeyi (1997) listeler.

Şubat 2001'de on yedi uygulayıcı Utah'ın Snowbird kentinde buluştu ve Manifesto'yu yazdı. Sonraki bildiriler onun üzerine kuruldu: 2005'te PM Declaration of Interdependence, 2009'da Software Craftsmanship Manifesto ve 2011'de Agile Alliance'ın *Guide to Agile Practices* kitabı; bu kitap 2016'da *Agile Glossary* olarak yeniden adlandırıldı.

### Uyarlanabilir ve öngörücü yaklaşımlar

Madde, öngörücü ve uyarlanabilir yaklaşımlar arasında bir süreklilik tanımlar. Öngörücü bir yöntem işin çoğunu başlamadan önce ayrıntılı planlar ve gereksinimler kararlı ve iyi anlaşıldığında iyi çalışır. Uyarlanabilir bir yöntem değişimi bekler ve kısa ufuklarla planlar. Maddede anılan Boehm ve Turner, her tarafın kendi "ev sahası" olduğunu, yani hiçbirinin her yerde doğru olmadığını savunur.

Bu, bir hizmet ekibi için önemlidir; çünkü işi karmaşıktır. Bir veri merkezi ağını değiştirmek öngörücü işe daha yakındır. Müşteriye dönük bir uygulamayı iyileştirmek uyarlanabilir işe daha yakındır. Yaklaşımı bütün kuruluş için bir kez değil, iş türü başına seçin.

### Yaygın yöntemler

Madde birçok yöntem listeler. En çok karşılaşacaklarınız:

| Yöntem | Ana vurgu | Ele alındığı yer |
|---|---|---|
| Scrum | Tanımlı roller, düzenli etkinlikler ve sabit bir ritim | Konu 1.4 — Teslimat Tahmini ve Planlama Metrikleri |
| Kanban | İşi görselleştirmek ve süren iş miktarını sınırlamak | Konu 1.5 — Kanban |
| Extreme Programming (XP) | Eşli programlama ve test güdümlü geliştirme gibi mühendislik uygulamaları | Konu 1.6 — Extreme Programming |
| Yalın yazılım geliştirme | İsrafı ortadan kaldırmak gibi yalın fikirleri yazılıma uygulamak | Konu 1.7 — Yalın Yazılım Geliştirme |
| Özellik güdümlü geliştirme, DSDM, Crystal ve uyarlanabilir yazılım geliştirme | Kendi rolleri ve uygulamaları olan, sürekli yazılım teslimine yönelik diğer hafif yöntemler | Bu konu |
| Scrumban | Scrum etkinlikleri ile Kanban akışının bir karışımı | Konu 1.4 — Teslimat Tahmini ve Planlama Metrikleri ve Konu 1.5 — Kanban |

Hiçbir yöntem "o" çevik yöntem değildir. Madde, Ken Schwaber'in ekiplerin, değişmesi gereken kuruluşun kendisi olduğunda mükemmel bir metodoloji arayarak başları belaya soktuğu görüşünü ve Bas Vodde'nin Scrum'ın ekiplerin yerel olarak genişlettiği temelleri sağladığı önerisini alıntılar.

### Yaygın uygulamalar

Madde, birçok çevik ekibin kullandığı uygulamaları listeler. Her birinin ne için olduğuyla birlikte bir seçki:

- **Kullanıcı hikâyeleri ve iş listeleri (backlog):** işi kullanıcının bakış açısından anlatın ve sırada ne yapılacağına dair öncelikli bir liste tutun.
- **Günlük ayakta toplantı (stand-up):** ilerlemeyi ve engelleri paylaşmak için, çoğunlukla yaklaşık 15 dakikalık kısa bir günlük toplantı.
- **Test güdümlü geliştirme (TDD) ve kabul testi güdümlü geliştirme (ATDD):** önce testleri yazın; böylece "bitti" işe başlamadan önce tanımlanır.
- **Sürekli entegrasyon (CI):** değişiklikleri sık birleştirin ve otomatik olarak derleyip test edin. Madde, terimi ilk kez Grady Booch'un 1991'de önerdiğini not eder.
- **Eşli programlama ve yeniden düzenleme (refactoring):** kaliteyi artırmak ve bilgiyi yaymak için iki kişi işi paylaşır ve kod, ne yaptığını değiştirmeden sürekli iyileştirilir.
- **Retrospektifler:** ekip, nasıl iyileşeceğine dair düzenli aralıklarla yansıtma yapar.

Bir hizmet ekibi için bunlardan üçü özel dikkat hak eder. Otomatik testler ve sürekli entegrasyon sık değişikliği güvenli kılar. Retrospektifler, ekibin çalışma biçimini iyileştirmesi için kalıcı bir yer sağlar. İş listeleri, hizmet iyileştirmelerinin yeni özelliklerle adil biçimde yarıştığı tek, sıralı bir liste sunar.

### Deneyim, ölçüm ve tuzaklar

Madde, 2002-2003'teki bir Shine Technologies anketi ve 2006'dan beri State of Agile anketi dahil anketlerin kalite, verimlilik ve iş memnuniyetinde algılanan kazanımlar bulduğunu bildirir. Ayrıca bir VersionOne anketinin yetersiz eğitimi başarısız uygulamaların en çok anılan nedeni olarak bulduğunu not eder ve ürün sahibi rolünü geliştirme ekibinin bir üyesiyle doldurmak ve sponsor desteğinden yoksun olmak gibi tuzakları listeler.

Bir ekibin "ne kadar çevik" olduğunu ölçmek, Nokia testi gibi çeşitli öz değerlendirmeler ve projeleri süre, risk, yenilik, çaba ve etkileşim üzerinden derecelendiren bir endeks doğurmuştur. Böyle her puana dikkat edin. Bir sayı sohbet başlatıcıdır ve puan için optimizasyon yapan bir ekip asıl amacı kaybedebilir.

### Büyük ölçekli, dağıtık ve düzenlemeye tabi iş

Madde, yaklaşık 20 geliştiricinin ötesine ya da lokasyonlar arasına ölçeklemenin zorluklar getirdiğini ve çeşitli çerçevelerin önerildiğini, ancak ne kadar iyi çalıştıkları konusunda görüşlerin ayrıldığını söyler (bkz. Konu 1.8 — Çevikliği Ölçeklendirme). Ayrıca tıbbi cihazlar, ilaç, finans, nükleer, otomotiv ve havacılık gibi düzenlemeye tabi alanların başlangıçta çeviklik için uygun olmadığının düşünüldüğünü ve artık uyarlamaların bulunduğunu bildirir. Listelediği kaygılar kalite güvencesi, emniyet ve güvenlik, izlenebilirlik ile doğrulama ve geçerlemedir.

Bunlar tam olarak hizmet yönetiminin kaygılarıdır. Bir düzenleyici ya da denetçi kanıt istediğinde, çevik bir ekip bunu zaten kullandığı araçlardan, örneğin sürüm kontrol geçmişinden, otomatik test sonuçlarından ve değişiklik kayıtlarından sağlayabilir (bkz. Konu 5.7 — Yönetişim, Risk ve Uyum).

### Bilinmesi gereken eleştiri

Steven Rakitin, 2001'de *IEEE Computer* dergisine yazdığı bir mektupta çevikliği "yazılım mühendisliği disiplinini baltalamaya yönelik bir girişim daha" olarak niteledi ve Manifesto'nun çalışan yazılım tercihini dokümantasyonu atlama ruhsatı olarak okudu. Savunucular, Scott Ambler'ın deyişiyle dokümantasyonun "tam yeterince iyi" olması gerektiğini söyler. Hizmet ekipleri her iki tarafı da bilir: çok az dokümantasyon devir teslimi ve olay müdahalesini yavaşlatır, çok fazlası ise eskir.

## İyi uygulamalar

1. **Yöntemi iş türüne uydurun.** Gereksinimlerin değiştiği yerde sürekli yazılım teslimini ve sık geri bildirimi, sabit oldukları ve hata maliyetinin yüksek olduğu yerde daha fazla önceden planlamayı kullanın. Bunu her iş türü için kararlaştırın ve koşullar değiştiğinde gözden geçirin.
2. **En küçük yararlı yığınla başlayın.** İşi günler içinde inşa edilebilen, test edilebilen ve yayımlanabilen parçalara bölün. Küçük yığınlar daha hızlı geri bildirim verir ve başarısız bir değişikliği anlamayı ve geri almayı kolaylaştırır.
3. **Sürümleri hızlandırmadan önce testi otomatikleştirin.** Otomatik testler olmadan sık sürümler riski kullanıcılarınıza taşır. Her değişiklikte çalışan ve yüksek sesle başarısız olan bir paket kurun ve bozuk bir derlemeyi ekibin ilk önceliği sayın.
4. **Sürekli entegre edin.** İşi ortak bir dala sık birleştirin ve otomatik olarak derleyin. Uzun ömürlü dallar, çakışmaları düzeltmesi pahalı hale gelene kadar gizler.
5. **"Bitti" tanımına operasyonu dahil edin.** Bir hikâye, izlenebilir, desteklenebilir ve geri alınabilir olana kadar bitmiş değildir. Bu kontrolleri bitti tanımınıza ekleyin ve operasyon çalışanlarından onu yazmaya yardım etmelerini isteyin (bkz. Konu 3.5 — Sürüm ve Dağıtım Yönetimi).
6. **Ekip başına tek sıralı bir iş listesi tutun.** Özellikleri, kusurları ve hizmet iyileştirmelerini aynı öncelikli listeye koyun ki açıkça yarışsınlar. Gizli yan kuyruklar, operasyonel işin sessizce aç kaldığı yerlerdir.
7. **Tam yeterince dokümantasyon yazın.** İnsanların kullandığı çalışma kılavuzları, hizmet tanımları ve mimari notlar gibi belgeleri tutun ve her birine bir sahip ve gözden geçirme tarihi verin. Gerisini silin. Bu, ağır belgelere dönmeden Rakitin'in kaygısını yanıtlar.
8. **Düzenli retrospektifler yapın ve onlara göre hareket edin.** Her birinden bir sahibi ve tarihi olan bir değişiklik seçin. Yalnızca tartışma üreten bir retrospektif bir ritüele dönüşür.
9. **Eğitime ve sponsorluğa yatırım yapın.** Wikipedia maddesindeki anket kanıtı, eğitim ve sponsor desteğini yaygın zayıf noktalar olarak işaret eder. Ekiplerden çalışma biçimlerini değiştirmelerini istemeden önce ikisini de planlayın.
10. **Uyarlayın ve nedenini söyleyin.** Bir yöntemi bağlamınıza uyarlayın ve neyi neden değiştirdiğinizi yazın. Bir uygulamayı, nedeni olmadan, yalnızca elverişsiz olduğu için değiştirmek, ekiplerin yararlardan uzaklaşmasının yoludur.
11. **Çeviklik puanlarını değil, sonuçları ölçün.** Bir değişikliğin teslim süresi, sürümlerin ne sıklıkla olaylara yol açtığı ve hizmetin ne kadar hızlı geri getirildiği gibi şeyleri izleyin (bkz. Konu 5.6 — Metrikler ve Ölçüm). Öz değerlendirmeleri yalnızca tartışma için ipucu olarak kullanın.
12. **Hizmet verisini geliştirmeye geri taşıyın.** Tekrarlayan olayları ve sorun kayıtlarını iş listesine besleyin; böylece geliştirme operasyondan öğrenir (bkz. Konu 3.3 — Sorun Yönetimi).

## Ekibinizle tartışılacak sorular

**Hangi çevik uygulamaları gerçekten kullanıyoruz, hangilerinin yalnızca adını biliyoruz?**

İzlediğinizi düşündüğünüz uygulamaları listeleyin: ayakta toplantılar, retrospektifler, iş listeleri, otomatik testler. Her biri için bir kararı en son ne zaman değiştirdiğini sorun. Kimsenin bir kararla ilişkilendiremediği uygulamalar ritüellerdir. Kolaylaştırıcı, suçlama ima etmeden kanıt istemelidir. İyileştirilecek ya da bırakılacak bir ritüel seçerek devam edin.

**Hangi işlerimiz için daha öngörücü bir yaklaşım daha akıllıca olurdu ve neden?**

Wikipedia maddesi her yaklaşımın bir "ev sahası" olduğunu bildirir. İnsanlardan yakın tarihli işi kararlı ve hızlı değişen olarak ayırmalarını isteyin. Tipik kararlı işler donanım yenilemeleri, veri merkezi taşımaları ve büyük sözleşme yenilemelerini içerir. Her durumda daha dikkatli bir planın neyi sağlayacağını sorun. Amaç tek bir tarzı her şeye uygulamaktan kaçınmaktır.

**Geliştirdiğimiz bir şeyin çalışmadığını ne kadar çabuk öğreniyoruz ve bunu ne hızlandırırdı?**

Bir değişikliği yazmaktan, kullanımda nasıl davrandığını öğrenmeye kadar uzanan yolu izleyin. Aşamaları ve beklemeleri sayın: gözden geçirme, derleme, test, sürüm, izleme. Ekibin en az hangi aşamaya güvendiğini sorun. Yanıt çoğunlukla elle yapılan bir test ya da tek bir kişiye bağlı bir sürüm adımıdır. Kısaltılacak bir aşama seçin ve kısaldığını nasıl anlayacağınız konusunda anlaşın.

**Bir denetçi ya da düzenleyici bizden ne görmek isterdi ve çalışma biçimimiz bunu zaten üretiyor mu?**

Denetim ya da güvenlik deneyimi olan birini katılmaya davet edin. Araçlarınızın zaten ürettiği kanıtı toplayın: değişiklik geçmişi, test sonuçları, onaylar. Sonra eksikleri listeleyin. Ekipler, otomatik kontrollerle sık küçük değişikliklerin seyrek büyük değişikliklerden daha iyi kanıt ürettiğini bulunca genellikle şaşırır. Boşlukları Konu 5.7 — Yönetişim, Risk ve Uyum'daki yönetişim tartışması için kaydedin.

**Dokümantasyonumuz insanlara nerede yardım ediyor ve nerede yalnızca yazmamız söylendiği için var?**

İnsanlara son ayda hangi belgeleri kullandıklarını sorun. Kullanılan ve güncel tutulan bir çalışma kılavuzu sayılır. Onaylandığı günden beri kimsenin okumadığı bir tasarım belgesi sayılmaz. Ekibin hangilerini tutacağına, hangilerini birleştireceğine ve hangilerini sileceğine karar vermesini sağlayın ve sahipler atayın. Bu, "tam yeterince iyi" fikrini uygulamanın güvenli bir yoludur.

**Çalışma biçimimizde öğrendiklerimiz yüzünden en son neyi değiştirdik ve bir sonraki değişiklik ne?**

Bir retrospektiften gelen en son somut değişikliği ve işe yarayıp yaramadığını sorun. Kimse bir tane adlandıramıyorsa, retrospektif işini yapmıyor demektir. Nedenine bakın: eylemler çok büyük olabilir, sahipleri olmayabilir ya da teslimat işiyle yarışıyor olabilir. Önümüzdeki iki hafta içinde yapılacak küçük bir değişiklik seçerek bitirin.

## Uygulamada: çevik bir ITIL örneği

Orta ölçekli bir çevrimiçi perakendecinin sipariş yönetim sistemini geliştiren on kişilik bir geliştirme ekibi ve onu işleten altı kişilik ayrı bir operasyon ekibi var. Geliştirme ekibi sprintleri ve iki haftada bir sürümü kullanmayı seçti. Operasyon ekibi her sürümü kısa bir notla ve Perşembe gecesi bir pencere içinde dağıtılması talebiyle alıyor. Operasyon çalışanları neyin değiştiğini ancak bir şey bozulunca öğrendiklerinden, geliştiriciler ise testte bulunan hiçbir şeyi düzeltmek için Perşembe penceresinin çok geç olduğundan şikâyet ediyor.

Ortak bir retrospektifte iki ekip yakın tarihli bir sürümü adım adım haritalar. Tek otomatik testlerin sipariş akışının yaklaşık yarısını kapsadığını, operasyon tarafında kimsenin sürümü Perşembe notundan önce görmediğini ve geri alma adımının hiç denenmediğini bulurlar. Üç değişiklik üzerinde anlaşırlar. Geliştirme ekibi bitti tanımına bir izleme kontrolü ve bir geri alma testi ekleyecek. Bir operasyon mühendisi her sprint gözden geçirmesine katılacak. Tam otomatik paketi geçen sürümler yalnızca Perşembe değil, hazır oldukları anda dağıtılacak.

Sonraki iki ayda, sonraki dört sürümden ikisi hafta ortasında dağıtılır. Operasyon mühendisi bir sprint gözden geçirmesinde eksik bir günlük mesajını yakalar; bu, sonraki bir olayda bir saatlik aramayı kurtarır. Her şey iyileşmez: otomatik paket hâlâ iade yolunu atlıyor ve bir iade hatası müşterilere ulaşıyor. Ekipler iade testlerini bir sonraki sprint'e ekler ve kapsam boşluklarını her ay gözden geçirmeyi kabul eder. Operasyon mühendisi ayrıca sprint gözden geçirmesine katılmanın, nöbet çizelgesinin izin vermediği zaman aldığını söyler; bu yüzden operasyon yöneticisi o mühendisin diğer görevlerinden bazılarını kaydırır.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri değişikliği güvenli kılan uygulamaların sahibidir: testler, sürekli entegrasyon, küçük yığınlar ve net bir bitti tanımı. Operasyonu işinizin bir müşterisi olarak görün. Bir sürümü işletmek için neye ihtiyaç duyduklarını sorun ve bir özellik gibi iş listesine ekleyin.

### Hizmet ve operasyon ekipleri

Operasyon çalışanları çevik uygulamaları kendi işlerinde kullanabilir: görünür bir iyileştirme iş listesi, olaylarla ilgili kısa geri bildirim döngüleri ve düzenli retrospektifler. Planlama ve gözden geçirme oturumlarına erken katılmayı isteyin. Hizmetlerin nasıl başarısız olduğuna dair bilgiyi getirin; bu, bir teslimat ekibinin alabileceği en yararlı girdidir.

### Liderlik ve yönetişim

Liderler, ekiplerin bu şekilde çalışmak için zaman ve eğitim alıp almayacağına karar verir. Wikipedia maddesindeki anket kanıtı, eğitim ve sponsorluğu yaygın zayıf noktalar olarak işaret eder. Hangi denetimlere ihtiyacınız olduğunu ve bir ekibin paralel bir süreç eklemek yerine kendi araçlarıyla bunları nasıl karşılayabileceğini sorun.

### Müşteriler ve kullanıcılar

Müşteriler çevik yöntemlerin yararını bir tören olarak değil, sabit bir ritimle görünür iyileşme olarak görür. Çalışan değişiklikleri düzenli olarak gözden geçirmeyi ve en çok neyin önemli olduğunun sorulmasını bekleyin. Karşılığında ekip, zamanında yanıtlara ve zamanla iyileşen küçük, kusurlu sürümleri kabul etme isteğine ihtiyaç duyar.

## Yaygın başarısızlık biçimleri

- **Mühendislik uygulamaları olmadan ritüelleri benimsemek.** Günlük toplantılar ve panolar ortaya çıkar, ama otomatik test yoktur; bu yüzden sürümler riskli kalır. Bunun yerine, törenlerin yanı sıra test, entegrasyon ve sürüm otomasyonuna yatırım yapın.
- **Karar haklarını değiştirmeden bir değişiklik sürecine "çevik" demek.** Ekipler hâlâ uzaktaki onayları bekler. Bunun yerine, kararları bilgisi olan kişilere taşıyın ve net sınırlar koyun.
- **Çevikliği dokümantasyonsuzluk bahanesi yapmak.** Devir teslimler ve olaylar zarar görür. Bunun yerine, insanların kullandığı kısa belgeleri tutun ve her birine bir sahip verin.
- **Eğitimi atlamak.** Wikipedia maddesindeki VersionOne bulgusu, yetersiz eğitimi başarısız uygulamaların en çok anılan nedeni olarak adlandırır. Bunun yerine, ekipleri ve liderleri değişimden önce ve değişim sırasında eğitin.
- **Ürün sahibi rolüne bir geliştirme ekibi üyesi koymak.** Madde bunu bir tuzak olarak listeler. Bunun yerine, işi temsil eden ve karar verecek zamanı olan birini seçin.
- **Bir çerçeveyi kopyalayarak ölçeklemek.** Anlaşılmadan kurulan büyük bir çerçeve süreç ekler ve ekipleri yavaşlatır. Bunun yerine, sahip olduğunuz sorunla başlayın ve yalnızca işe yarayanı benimseyin (bkz. Konu 1.8 — Çevikliği Ölçeklendirme).
- **Bir çeviklik puanının peşinden koşmak.** Ekipler metrik için optimizasyon yapar. Bunun yerine, teslim süresi, sürüm hataları ve hizmeti geri getirme süresi gibi sonuçları izleyin.
- **Geliştirme ile operasyonu ayrı tutmak.** Teslimat ekibi gönderir, operasyon ekibi devralır. Bunun yerine, onları ortak planlamaya, gözden geçirmelere ve olay öğrenmesine dahil edin (bkz. Konu 5.2 — DevOps).

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Sürekli yazılım teslimi | İş büyük sürümlerle teslim edilir | Bazı ekipler kısa döngülerle teslim eder | Ekipler ortak bir teslimat ritmini ve bir bitti tanımını paylaşır | Teslim süresi ve sürüm sonuçları ölçülür ve gözden geçirilir | Sürüm ritimleri ekipler ve tedarikçiler arasında eşgüdümlenir |
| Mühendislik uygulamaları | Test ve derlemeler çoğunlukla elle yapılır | Bazı ekiplerin otomatik testleri ve derlemeleri vardır | Ortak bir boru hattı her değişiklikte testleri çalıştırır | Test kapsamı ve başarısızlık oranları izlenir ve boşluklar giderilir | Boru hatları ve uygulamalar ortak kanıta dayanarak ekipler arasında iyileştirilir |
| İş listesi ve önceliklendirme | Talepler e-postayla ve plansız gelir | Ekipler kendi iş listelerini tutar | Her ekibin hizmet işini de içeren tek sıralı bir iş listesi vardır | İş listesi akışı ve yaşı paydaşlarla gözden geçirilir | Öncelikler ekipler, müşteriler ve tedarikçiler arasında hizalanır |
| Öğrenme ve uyum | Gözden geçirmeler yalnızca büyük arızalardan sonra yapılır | Bazı ekipler retrospektif yapar | Tüm ekipler düzenli retrospektif yapar ve eylemleri kaydeder | Eylemler tamamlanana kadar izlenir ve etkileri kontrol edilir | Dersler merkezi yönlendirme olmadan ekipler arasında ve politikaya taşınır |

## Kontrol listesi

- [ ] Ekip hangi çevik yöntemi ya da uygulamaları kullandığını ve neden seçtiğini söyleyebiliyor.
- [ ] İş, öngörücü ve uyarlanabilir türlere ayrılmış ve her biri için belirtilmiş bir yaklaşım var.
- [ ] Otomatik testler her değişiklikte çalışıyor ve başarısız bir derleme hattı durduruyor.
- [ ] Bitti tanımımız izlemeyi, destek notlarını ve sınanmış bir geri almayı içeriyor.
- [ ] Her ekibin hizmet iyileştirmelerini ve kusurları içeren tek sıralı bir iş listesi var.
- [ ] Çalışma kılavuzlarının ve hizmet tanımlarının sahipleri ve gözden geçirme tarihleri var.
- [ ] Retrospektifler düzenli bir ritimle yapılıyor ve her biri sahipli tek bir eylemle bitiyor.
- [ ] Ekipler ve liderler, onlardan istediğimiz çalışma biçimi konusunda eğitim aldı.
- [ ] Denetçilerin hangi kanıta ihtiyaç duyduğunu ve araçlarımızın bunu nasıl sağladığını biliyoruz.
- [ ] Teslim süresi ve hizmeti geri getirme süresi gibi sonuç ölçüleri düzenli gözden geçiriliyor.

## Yapay zeka istemleri

**Amaç: mevcut uygulamalarınızı yaygın çevik uygulamalarla eşleştirmek ve boşlukları bulmak.**

```text
You are helping a team understand which agile software development practices it actually uses.

Practices to consider: user stories and backlogs, daily stand-ups, retrospectives, test-driven development, continuous integration, pair programming, refactoring, definition of done, regular reviews with customers.

Our team: [team size and what you build and run].
What we do today, in our own words: [paste a short description of a typical week, including meetings, tools, and how a change reaches production].

For each practice, say whether the description shows it in use, partly in use, or not mentioned, and quote the words you based that on. Do not assume a practice exists if it is not described. Then list three questions I should ask my team to fill gaps. Ask me clarifying questions first if the description is too thin, and list what you are unsure of.
```

**Amaç: operasyonu da içeren bir bitti tanımı taslağı hazırlamak.**

```text
Help us write a definition of done for [type of work, e.g. "backend changes to our order service"] that covers both building and running the service.

Our current definition of done is: [paste it, or write "none"].
Things operations staff tell us they need before they accept a release: [paste a list, or write "unknown"].
Rules we must follow: [list any known audit, security, or safety rules, or write "none known"].

Produce a checklist of 8 to 12 items, grouped as build quality, release readiness, and operational readiness. Mark each item that you added by assumption. Do not claim that any standard requires an item unless I have pasted its text. Ask me clarifying questions first, and list what you are unsure of.
```

**Amaç: çevik araçlarınızdan bir denetçi için kanıt hazırlamak.**

```text
An auditor has asked: [paste the question, e.g. "show me how changes are reviewed and approved"].

Our tools and records: [list your version control, build, test, ticket, and release tools, and what each records].
Our practice: [describe how a change goes from idea to production].

List what evidence each tool already produces that relates to the question, what gaps remain, and three lightweight ways to close each gap. Do not state that any law or standard requires something unless I have pasted its text. Separate facts from assumptions, and list what you are unsure of.
```

**Amaç: ekibinizin çevik uygulamaları nasıl benimsediği üzerine bir retrospektif planlamak.**

```text
Plan a 60-minute retrospective for a team of [number] people who are [adopting / improving] agile practices. The main problem right now is [problem].

Include: a timed agenda, a way to gather facts first, a short discussion of two or three of these questions: [paste questions from the "Questions to discuss" section], and a closing step that records exactly one action with an owner and a date.

Keep the plan free of any specific tool. If anything is missing, ask me clarifying questions first, and list what you are unsure of.
```

## Yapay zeka becerileri

- [scrum](../../../../skills/scrum/SKILL.md): bir Scrum ekibinin rollerini, etkinliklerini ve çıktılarını kurmak ya da gözden geçirmek için kullanın.
- [kanban](../../../../skills/kanban/SKILL.md): bir hizmet ya da operasyon ekibi için süren iş limitli görsel bir pano tasarlamak için kullanın.
- [extreme-programming](../../../../skills/extreme-programming/SKILL.md): test güdümlü geliştirme ve sürekli entegrasyon gibi mühendislik uygulamalarını gözden geçirmek ya da benimsemek için kullanın.
- [user-story](../../../../skills/user-story/SKILL.md): operasyonel ihtiyaçları da içeren kabul ölçütleriyle kullanıcı hikâyeleri yazmak için kullanın.
- [agile-reflection](../../../../skills/agile-reflection/SKILL.md): sahipli tek bir değişiklikle biten bir retrospektif yürütmek için kullanın.

## Temel kaynaklar

- **Manifesto for Agile Software Development** ve **Principles behind the Agile Manifesto** (agilemanifesto.org): değerlerin ve ilkelerin birincil ifadesi.
- **Agile software development** (Wikipedia): tarihçe, yöntemler, uygulamalar, benimseme ve eleştiriyi, birçok alıntılanmış kaynakla kapsayan geniş bir genel bakış.
- **Agile Glossary** (Agile Alliance): Manifesto'dan doğan topluluk tarafından sürdürülen çevik uygulama ve terim tanımları.

## Kaynakça

1. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
2. Manifesto for Agile Software Development — Beck et al., agilemanifesto.org — https://agilemanifesto.org/
3. Principles behind the Agile Manifesto — Beck et al., agilemanifesto.org — https://agilemanifesto.org/principles.html
4. Waterfall model — Wikipedia — https://en.wikipedia.org/wiki/Waterfall_model
5. Scrum (software development) — Wikipedia — https://en.wikipedia.org/wiki/Scrum_(software_development)
6. Extreme programming — Wikipedia — https://en.wikipedia.org/wiki/Extreme_programming
7. Kanban (development) — Wikipedia — https://en.wikipedia.org/wiki/Kanban_(development)
8. Test-driven development — Wikipedia — https://en.wikipedia.org/wiki/Test-driven_development
9. Continuous integration — Wikipedia — https://en.wikipedia.org/wiki/Continuous_integration
10. Feature-driven development — Wikipedia — https://en.wikipedia.org/wiki/Feature-driven_development
11. Dynamic systems development method — Wikipedia — https://en.wikipedia.org/wiki/Dynamic_systems_development_method
12. Agile Glossary — Agile Alliance — https://www.agilealliance.org/agile101/agile-glossary/
