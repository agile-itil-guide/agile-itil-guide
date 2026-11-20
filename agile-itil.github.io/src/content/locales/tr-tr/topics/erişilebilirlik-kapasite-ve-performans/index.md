# Erişilebilirlik, Kapasite ve Performans

**Erişilebilirlik, kapasite ve performans, bir hizmetin kullanıcılar ihtiyaç duyduğunda orada olup olmadığının, yeterince büyük ve yeterince hızlı olup olmadığının üç görünümüdür; çevik yaklaşım, hedefleri kullanıcı ihtiyaçlarından seçmek, bunları dürüstçe fiyatlandırmak ve talep gelmeden önce sınamaktır.**

## Bu neden önemli

Kullanıcılar bu üçünü ayırmaz. "Ayakta" olan ama kullanılamayacak kadar yavaş bir hizmet onları yarı yolda bırakmıştır; sakin bir günde hızlı olup zirvede çöken bir hizmet ise onlara en çok ihtiyaç duydukları anda başarısız olmuştur. Erişilebilirliğe, kapasiteye ve performansa ayrı ayrı bakan ekipler, bunların birbirini etkileme biçimlerini çoğu zaman kaçırır: kapasite eklemek maliyeti ve karmaşıklığı değiştirir, kusursuz erişilebilirliğin peşinde koşmak ne kadar hızlı değişiklik yapabileceğinizi sınırlar ve hız için ayar yapmak dayanıklılığı azaltabilir.

Çevik ekipler sorunun belirli bir sürümüyle karşılaşır. Hizmeti sık değiştirirler ve her değişiklik performansı ya da kaynak ihtiyaçlarını kimsenin sınamadığı biçimlerde değiştirebilir. Ayrıca kısa zaman ufuklarıyla çalışma eğilimindedirler; bu yüzden donanım, sözleşmeler ya da lisanslar gibi ayarlanması aylar süren kapasite ihtiyaçları gözden kaçabilir. Bu konudaki uygulamalar, uzun vadeli planlamaya salt kendi uğruna dönmeden ileriye bakmanın bir yolunu sunar.

Google'ın *Site Reliability Engineering* kitabı, "Embracing Risk" bölümünde, erişilebilirliğin ekonomisi konusunda açık bir kaynaktır: yaklaşımının %100 güvenilirliği hedeflemediğini söyler, çünkü belirli bir noktadan sonra kararlılığı azamileştirmek yeni özelliklerin ne kadar hızlı geliştirilebileceğini sınırlar ve güvenilirlik maliyetleri dik biçimde artar. [Kapasite planlamasına ilişkin Wikipedia maddesi](https://en.wikipedia.org/wiki/Capacity_planning) genel tanımlar ve stratejiler verir. İkisi de kısmidir ve burada kullanılan ITIL sözcük dağarcığı, bu rehberin çerçeve sahibinin metnine karşı doğrulayamadığı, yaygın olarak yayımlanmış betimlemelerden gelir.

## Temel kavramlar

### Erişilebilirlik

**Erişilebilirlik (availability)**, bir hizmetin kullanıcıların ihtiyaç duyduğunu, ihtiyaç duyduklarında yapabilme yeteneğidir. Bunu ifade etmenin yaygın bir yolu, bir dönem üzerinden yüzde olarak vermektir. SRE bölümü onu ölçmenin iki yolunu not eder. Tek bir sistem için erişilebilirlik zamana dayanır: %99,99, yılda yaklaşık 52,56 dakikalık plansız kesintiye izin verir. Her zaman kısmen ayakta olan dağıtık hizmetler için, yuvarlanan bir pencerede istek başarı oranı olarak ölçmek daha iyidir; bölümün örneği, günde 2,5 milyon isteği ve %99,99 hedefi olan, 250'ye kadar hataya izin veren bir hizmettir. Bölüm plansız kesintiye odaklanır. Planlı kesinti, kullanıcılarla ayrı bir anlaşma gerektirir.

### Her ek dokuzun bedeli

Bölüm, güvenilirlik maliyetlerinin doğrusal olmayan biçimde arttığını söyler: bir ek dokuz, önceki artışın 100 katına mal olabilir; buna yedek kaynaklar ve mühendislerin kullanıcıya dönük özellikler geliştirmemesinin fırsat maliyeti dahildir. Bir örnek verir: 1 milyon dolar gelirli bir hizmette erişilebilirliği %99,9'dan %99,99'a çıkarmak yaklaşık 900 dolarlık değere eşdeğerdir; dolayısıyla yatırım yalnızca ek dokuz bundan daha ucuza mal olursa karşılığını verir. Sayılar kaynağın örneğidir ve sizinkiler kendi gelirinizden ya da değerinizden gelmelidir. İlke geçerlidir: kullanıcıların ihtiyaç duyduğu erişilebilirliği seçin ve bunun ötesindeki her şeyi fiyatlandırın.

### Risk toleransı

Bölüm, iş hedeflerini açık hedeflere dönüştürmek için ürün sahipleriyle çalışmayı betimler. Etkenler arasında gereken erişilebilirlik, arızaların biçimi (sürekli düşük bir hata oranı ile ara sıra tam kesintiler; veri ifşası özellikle ağırdır), maliyet ve gecikme gibi diğer ölçüler yer alır. Birçok istemciye hizmet veren altyapının açıkça tanımlanmış hizmet seviyelerinde sunulabileceğini, böylece her istemcinin ihtiyaçlarını karşılayan en ucuz seviyeyi seçebileceğini not eder.

### Hata bütçeleri

Bölüm hata bütçesini, hız üzerinden ölçülen ürün ekipleri ile güvenilirlik üzerinden ölçülen güvenilirlik ekipleri arasında paylaşılan, nesnel bir ölçü olarak açıklar. Bütçe kaldığı sürece sürümler devam eder. Bütçe tükendiğinde sürümler yavaşlar ve çaba güvenilirliğe kayar (bkz. Konu 3.7 — Hizmet Seviyesi Yönetimi).

### Kapasite

Wikipedia maddesi kapasite planlamasını, bir kuruluşun değişen talebi karşılamak için ihtiyaç duyduğu üretim kapasitesini belirleme olarak tanımlar ve BT'de bunun kapasite yönetimiyle eş anlamlı olduğunu, yani gelecek bir dönemde gereken depolama, donanım, yazılım ve bağlantı kaynaklarının tahmin edilmesi olduğunu söyler. Madde, mümkün olan azami çıktı olan **tasarım kapasitesini (design capacity)** kısıtlardan sonraki çıktı olan **etkin kapasiteden (effective capacity)** ayırır. Pratikte, her zaman tasarım rakamından düşük olan etkin kapasiteye göre planlayın.

### Kapasite stratejileri

Madde kapasite eklemek için dört strateji betimler:

| Strateji | Ne anlama gelir | Ödünleşim |
|---|---|---|
| **Önde gitme (Lead)** | Talepten önce kapasite eklemek | İyi hizmet ve kısa tedarik süreleri, ancak talep öngörülemezse risklidir |
| **Geriden gelme (Lag)** | Kapasiteyi yalnızca tam kapasitede ya da ötesinde çalıştıktan sonra eklemek | Gereğinden fazla inşa etme riski düşük, ancak müşteri kaybedilebilir |
| **Eşleştirme (Match)** | Talep değiştikçe kapasiteyi küçük artışlarla eklemek | Dengeli, iyi izleme gerektirir |
| **Uyarlama (Adjustment)** | Talep ya da mimari değiştikçe kapasiteyi küçük ya da büyük miktarlarda eklemek veya azaltmak | Esnek, hızlı provizyon gerektirir |

Madde, günlerden yıllara uzanan kısa, orta ve uzun vadeli planlamayı (operasyonel, taktik ve stratejik) betimler. Bir bulut ortamında "eşleştirme" ve "uyarlama" çoğunlukla daha kolaydır, çünkü kaynaklar hızla eklenebilir; ancak maliyet ve sözleşmelerin yine de planlanması gerekir (bkz. Konu 4.5 — BT Mali Yönetimi ve FinOps).

### Performans

**Performans (performance)**, hizmetin ne kadar hızlı ve ne kadar iyi yanıt verdiğidir. SRE kitabının izleme bölümü gecikmeyi, trafiği, hataları ve doygunluğu ölçmeyi önerir ve ortalamaların yavaş aykırı değerleri gizlediği konusunda uyarır (bkz. Konu 3.10 — İzleme ve Etkinlik Yönetimi). Doygunluk, yani hizmetin ne kadar "dolu" olduğu, performansı kapasiteye bağlar: bölüm performansın çoğunlukla %100 kullanıma ulaşmadan bozulduğunu not eder.

### Üçünün birbiriyle etkileşimi

- Daha fazla kapasite, bir maliyetle erişilebilirliği ve performansı artırabilir.
- Yüksek erişilebilirlik hedefleri genellikle yedeklilik gerektirir, ki bu fazladan kapasitedir.
- Zirve performansı için ayar yapmak, arıza için payı azaltabilir.
- Hizmette yapılan değişiklikler üçünü de değiştirir; sınamanın önemli olmasının nedeni budur.

Yararlı bir disiplin, her hizmet için hedefleri birlikte belirtmektir: ne kadar erişilebilir, ne kadar hızlı ve ne kadar yük taşımalı.

### Talep ve tahmin

Kapasite talebe bağlıdır. Talep kullanıcılardan ve işten gelir: pazarlama kampanyaları, mevsimsel zirveler, yeni müşteriler. İş, gelecek hakkında BT'den daha fazla şey bilir, bu yüzden sorun. Tek sayılar yerine aralıklarla planlayın ve tahmini düzenli olarak yeniden ele alın (aşağıdaki talep tahmini becerisine bakın).

### Sınama

Kapasite ve performans iddiaları sınanana kadar birer hipotezdir. Yük sınaması ve performans sınaması, hizmetin nasıl davrandığını görmek için gerçekçi talep uygular; kaos sınaması (chaos testing) ise erişilebilirliğin korunup korunmadığını görmek için arızalar ortaya çıkarır. Bunlar teslimat hattının parçası olabilir.

### Kaynakların sınırları

Kapasite planlamasına ilişkin Wikipedia maddesi ITIL kapasite yönetiminden söz etmez ve kapasite, performans ve erişilebilirlik arasındaki ilişkiyi çözümlemez; varlıklara ilişkin bölümü de atıfsız olarak işaretlenmiştir. SRE bölümü, kendine özgü ekonomisi olan çok büyük bir kuruluşun uygulamalarını betimler. Bunları sayılar için değil, ilkeler için kullanın.

## İyi uygulamalar

1. **Erişilebilirlik, performans ve yük hedeflerini birlikte belirtin.** Her hizmet için ne kadar erişilebilir olması, ne kadar hızlı yanıt vermesi ve ne kadar yük taşıması gerektiğini yazın. Bunları kullanıcı ihtiyaçlarına dayandırın ve hizmet sahibi ve müşterilerle uzlaşın.
2. **Hedefleri fiyatlandırın.** Ek bir erişilebilirlik ya da hız seviyesinin para ve gecikmiş özellikler olarak neye mal olduğunu tahmin edin. Bunu kullanıcıların ve işin kazanacağıyla karşılaştırın. Bir kitaptaki örneği değil, kendi rakamlarınızı kullanın.
3. **Erişilebilirliği hizmete uyan bir biçimde ölçün.** Her zaman kısmen ayakta olan hizmetler için SRE bölümünün yaptığı gibi yuvarlanan bir pencerede başarı oranını kullanın. Basit sistemler için zamana dayalı ölçüler kullanın. Plansız ve planlı kesintiyi ayrı sayın.
4. **Etkin kapasiteye göre planlayın.** Ek yük, bileşen arızaları ve bakım gibi gerçek kısıtlardan sonra hizmetin neyi taşıyabileceğini tahmin edin. Bir pay bırakın.
5. **Kapasite stratejisini bilinçli seçin.** Her kaynak için tedarik sürelerine, kıtlığın maliyetine ve gereğinden fazla inşa etmenin maliyetine dayanarak önde gitme, geriden gelme ya da eşleştirmeye karar verin. Seçimi yazın ve yeniden ele alın.
6. **Talebi işe sorun.** Kampanyaları, lansmanları ve mevsimsel zirveleri öğrenmek için pazarlama, satış ve operasyon liderleriyle düzenli bir döngüde buluşun. Beklenen yükü aralıklarla kaydedin.
7. **Doygunluğu izleyin.** Kilit kaynakların ne kadar dolu olduğunu izleyin ve performansın bozulduğu noktadan çok önce uyarılar belirleyin. Hizmetinizin yavaşlamaya başladığı seviyeyi bilin.
8. **Zirveden önce sınayın.** Bilinen zirvelerden önce ve önemli değişikliklerden sonra gerçek trafiğe benzeyen yük ve performans sınamaları yapın. Bulduğunuzu zaman varken düzeltin.
9. **Yalnızca yükü değil, arızayı da sınayın.** Güvenli bir ortamda bir bileşeni, bir bölgeyi ya da bir tedarikçiyi kaybetmeyi deneyin ve erişilebilirliğin korunup korunmadığını görün (aşağıdaki kaos sınaması becerisine bakın).
10. **Kapasiteyi değişiklik ve sürüm işine dahil edin.** Tasarımda ve gözden geçirmede bir değişikliğin kaynak ihtiyaçlarını değiştirip değiştirmediğini sorun. Önemli yollar için teslimat hattına performans denetimleri ekleyin (bkz. Konu 3.5 — Sürüm ve Dağıtım Yönetimi).
11. **Ödünleşimleri çözmek için hata bütçesini kullanın.** Bütçe varken onu değişikliğe harcayın. Tükendiğinde çabayı güvenilirliğe ve kapasiteye harcayın. Kuralı teslimat ve operasyonla birlikte gözden geçirin.
12. **Tahminleri gerçekleşenlerle karşılaştırın.** Her çeyrekte öngörülen ve gerçekleşen talebi karşılaştırın ve yönteminizi ayarlayın. Sürprizleri bilgi olarak ele alın.

## Ekibinizle tartışılacak sorular

**Kullanıcılarımızın erişilebilirlik, hız ve kapasitede gerçekten neye ihtiyacı var ve buna kim karar verdi?**

Mevcut hedefleri ve nereden geldiklerini isteyin. Çoğu zaman bunlar uzun zaman önce ya da ekip tarafından kullanıcılara sorulmadan belirlenmiştir. Kullanıcılara ve müşterilere neyin en çok acıttığını sorun. Hedeflerin uyuşup uyuşmadığını tartışın. Kolaylaştırıcı, hedef bir basamak daha düşük olsaydı ne olacağını ve bunun neyi serbest bırakacağını sorabilir.

**Bir sonraki dokuz bize neye mal oluyor?**

Yüksek erişilebilirlik hedefi olan bir hizmet seçin. Bunu bir basamak yükseltmenin ya da düşürmenin para ve gecikmiş iş olarak neye mal olacağını tahmin edin. Kullanıcılar için değerle karşılaştırın. SRE bölümünün örneği, aritmetiğin daha yüksek bir hedefe karşı ne kadar hızlı döndüğünü gösterir. Hesabı kendi sayılarınızla yapın ve varsayımları kaydedin.

**Bildiğimiz bir sonraki talep zirvesi nedir ve hazırlanmak için ne yaptık?**

Bilinen zirveleri listeleyin: bir kampanya, bir son tarih, mevsimsel bir yoğunluk. Her biri için beklenen yükü kimin bildiğini ve hizmetin o seviyede sınanıp sınanmadığını sorun. Çoğu zaman kimse sormamıştır. Sayıları toplayacak bir kişi ve sınama için bir tarih üzerinde anlaşın.

**Hizmetimiz doygunluğa en çok nerede yakın ve oraya vardığında ne oluyor?**

En yoğun kullanılan kaynağı sorun. Eğilime bakın. Hizmetin bu sınırda ne yaptığını sorun: yavaşlıyor, hata veriyor ya da arızalanıyor mu. Kimse bilmiyorsa sınayın. Harekete geçilecek bir eşik ve bunun için bir uyarı seçin.

**Son birkaç değişikliğimizden hangisi performansı ya da kapasiteyi etkiledi ve bunu önceden biliyor muyduk?**

Son değişiklikleri gözden geçirin ve performansın nasıl denetlendiğini sorun. Denetlenmediyse hafif bir denetimin ne olacağını tartışın. Tipik seçenekler kritik yolda bir sınama ya da izlemeli bir kanarya (canary) sürümüdür. Bir sonraki sürüm için birini kabul edin.

**Bir bileşen şu anda arızalansa erişilebilirliğe ne olurdu?**

Kilit bir hizmeti alın ve bir veritabanının, bir bölgenin ya da bir tedarikçinin arızasını izleyin. Tasarımın neyi varsaydığını ve neyin sınandığını sorun. Varsayım ile kanıt arasındaki boşluklar risktir. Güvenli bir ortamda bir kontrollü arıza sınaması planlayın.

## Uygulamada: çevik bir ITIL örneği

Ulusal bir emeklilik kurumu, vatandaşların haklarını kontrol edip formlar gönderdiği bir çevrim içi hizmet işletiyor. Hizmetin yıllık ekstrelerin yayımlanmasından sonraki haftalar dışında sakin bir yılı vardır; o haftalarda trafik normal seviyenin birkaç katına çıkar. Geçen yıl hizmet, birçok kullanıcının vazgeçeceği kadar yavaşladı ve çağrı merkezi bunaldı. Dokuz kişilik platform ekibi ve operasyon müdürü, bunun tekrarlanmasını istemiyor.

Ekip, iletişim ofisinden beklenen yükü isteyerek başlıyor. Ofis ekstrelerin iki parti halinde gönderileceğini söylüyor ve tarihleri veriyor, ancak rakam vermiyor. Ekip aralığı geçen yılın verilerinden tahmin ediyor ve bir hedef belirliyor: formlar sayfası beklenen zirve için kabul edilebilir bir sürede yanıt vermeli ve hizmet iki parti boyunca erişilebilir kalmalı. Üretimin bir kopyasında yük sınaması yapıyorlar ve doygunluğa ilk ulaşan kaynağın, öngörülen zirvenin hayli altında, veritabanı olduğunu görüyorlar. Kapasite eklemenin tedarik süresi uzun olduğu için veritabanında "önde gitme", dakikalar içinde eklenebilen web sunucularında ise "eşleştirme" stratejisini benimsiyorlar. Bir arıza sınaması, bir veritabanı düğümünü kaybetmenin kapasiteyi yarıya indirdiğini, bunun zirvede kabul edilemez olacağını gösteriyor; bu yüzden bir yedek ekliyorlar.

Zirvede hizmet ayakta kalıyor ve ilk partide yanıt süreleri korunuyor. İkinci partide kimsenin sınamadığı bir ödeme onayı bileşeni yük altında yavaşlıyor ve bazı kullanıcılar gecikmeler görüyor. Ekip bu bağımlılığın sınırını bilmiyordu ve ikinci partinin daha büyük olacağı kendilerine söylenmemişti. Bileşeni bir sonraki yük sınamasına ekliyor, iletişim ofisinden her partinin hacmini daha erken istiyor ve tahmin sürecini bir sonraki çeyrekte gözden geçirmeyi kabul ediyor.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri tasarım ve değişiklik yoluyla üçünü de etkiler. Performansı ve kapasiteyi tasarım gözden geçirmelerine ve teslimat hattına dahil edin. Yükü değiştiren değişiklikleri operasyona bildirin ve beklenen talebi işe sorun.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri genellikle izleme ve kapasite planlarını taşır. Doygunluğu ve eğilimi izleyin, kaynaklar için tedarik sürelerinin bir görünümünü tutun ve planlamaya kanıt getirin. İşin, her erişilebilirlik seviyesinin neye mal olduğunu anlamasına yardımcı olun.

### Liderlik ve yönetişim

Liderler güvenilirlik ve hız için ödemeye razı oldukları bedeli belirler. Maliyetleriyle birlikte kullanıcı ihtiyaçlarına uyan hedefler isteyin ve kusursuz erişilebilirliğin akla yatkın bir hedef olmadığını kabul edin. Bilinen zirvelerden önce sınamayı ve önemli olduğu yerde dayanıklılık bütçesini destekleyin.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar sonucu hisseder. Bir kampanya ya da son tarih gibi ek yük beklediğinizde ve hız ile erişilebilirlikte sizin için en önemli olanın ne olduğunu sağlayıcıya söyleyin. Yavaşlığı da kesintiler kadar bildirin, çünkü sizin açınızdan ikisi de arızadır.

## Yaygın başarısızlık biçimleri

- **Alışkanlıktan gelen hedefler.** Nedenini sormadan "beş dokuz" talep edilir. Bunun yerine hedefleri kullanıcı ihtiyaçlarından türetin ve fiyatlandırın.
- **Sürpriz zirveler.** İş bir kampanyayı bilir, BT bilmez. Bunun yerine düzenli bir döngüde buluşun ve beklenen yükü kaydedin.
- **Performans için ortalamalar.** Yavaş aykırı değerler görülmez. Bunun yerine yüksek yüzdeliklere ve doygunluğa bakın.
- **Yalnızca sorundan sonra eklenen kapasite.** Geriden gelme stratejisi kazara kullanılır. Bunun yerine tedarik sürelerine dayanarak bilinçli bir strateji seçin.
- **Sınanmamış dayanıklılık.** Yedeklilik kâğıt üzerinde vardır. Bunun yerine bileşen arızalarını güvenli bir ortamda sınayın.
- **Performans denetimi olmayan değişiklikler.** Bir sürüm hızı bozar. Bunun yerine önemli yollar için teslimat hattına denetimler ekleyin.
- **Bağımlılıkları unutmak.** Üçüncü taraf bir bileşen tüm hizmeti sınırlar. Bunun yerine bağımlılıkları listeleyin ve sınayın.
- **Tahmini sabit saymak.** Planlar hatayı yok sayar. Bunun yerine aralıklar kullanın ve tahminleri gerçekleşenlerle karşılaştırın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Hedefler ve maliyet | Hedefler gayriresmî ya da kopyalanmıştır | Bazı hizmetlerin belirtilmiş hedefleri vardır | Hizmetlerin bilinen maliyetlerle uzlaşılmış erişilebilirlik, performans ve yük hedefleri vardır | Hedefler ve maliyetler sonuçlara karşı gözden geçirilir | Hedefler müşteriler ve tedarikçilerle birlikte belirlenir ve kanıta göre ayarlanır |
| Talep ve kapasite planlaması | Kapasite sorundan sonra eklenir | Bazı ekipler bilinen zirveleri tahmin eder | Talep işten bir döngüde toplanır, belirtilmiş bir kapasite stratejisiyle | Tahmin doğruluğu izlenir ve yöntemler geliştirilir | Planlama ekipler, tedarikçiler ve iş arasında eşgüdümlüdür |
| Sınama | Yük ya da arıza için az sınama | Büyük etkinliklerden önce bazı sınamalar | Yük ve arıza sınamaları kilit hizmetler için rutindir | Sınama sonuçları izlenen iyileştirmeleri yönlendirir | Sınamalar birbirine bağımlı hizmetler arasında paylaşılır ve eşgüdümlenir |
| İzleme ve yanıt | Sorunlar geç fark edilir | Bazı doygunluk izlenir | Doygunluk, gecikme ve hatalar sınırlardan önce uyarılarla izlenir | Eğilimler ve eşikler verilerden ayarlanır | Sinyaller ve yanıtlar ekipler ve tedarikçiler arasında eşgüdümlüdür |

## Kontrol listesi

- [ ] Her hizmetin erişilebilirlik, performans ve yük için kaynaklarıyla birlikte belirtilmiş hedefleri var.
- [ ] Bir sonraki erişilebilirlik seviyesinin neye mal olacağını tahmin ettik.
- [ ] Her hizmet için erişilebilirliğin nasıl ölçüldüğünü ve neyin kesinti sayıldığını biliyoruz.
- [ ] Her kilit kaynak için bir kapasite stratejisi seçtik.
- [ ] Beklenen talebi öğrenmek için işle düzenli olarak buluşuyoruz.
- [ ] Kilit kaynakların doygunluğu, sınırlardan önce uyarılarla izleniyor.
- [ ] Bilinen son zirveden önce yük sınamaları yapıldı.
- [ ] En az bir kilit bileşenin arızası güvenli bir ortamda sınandı.
- [ ] Performansı ya da kapasiteyi etkileyen değişiklikler gözden geçirmede işaretleniyor.
- [ ] Tahminler her çeyrekte gerçekleşen taleple karşılaştırılıyor.

## Yapay zeka istemleri

**Amaç: ölçülmüş verileri kapasite payı görünümüne dönüştürmek.**

```text
Here are the measurements for [resource, e.g. "database CPU"] for [service] over [period]: [paste real values or summary figures such as daily peak and average].
Known limit at which performance degrades, if you know it: [paste, or write "unknown"].
Expected demand change: [describe, with source].

Using only my data, describe the trend and how much headroom there appears to be at the observed peak, in plain words. Show how headroom would change if demand grew by the amounts I gave. Do not invent limits or growth rates. Say what extra data would make the analysis more reliable, and list what you are unsure of.
```

**Amaç: daha yüksek bir erişilebilirlik hedefini fiyatlandırmak.**

```text
Help me compare the cost and value of raising the availability target for [service] from [current target] to [proposed target].

What the service is worth, with source (revenue, cost of an outage, or other value; use only figures I provide): [paste].
What the extra availability would require (redundancy, staff, tools), with cost estimates I have: [paste, or write "unknown"].
Current measured availability: [paste].

Calculate the allowed unplanned downtime or error count at each target using only the numbers I gave, show the difference, and compare with the value and cost figures if I provided them. State your assumptions. Do not invent costs or revenue. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bilinen bir zirveden önce bir yük sınaması planlamak.**

```text
Plan a load test for [service] before this event: [describe the peak, with date and source of the expected load].

Architecture, in brief: [describe components, dependencies, and suppliers].
Expected load range, with the source: [paste].
Test environment available: [describe].

Give a plan with: goals, what to measure (latency distribution, errors, saturation), scenarios to run, how to ramp up, what to do with results, and risks to production or to suppliers (for example agreements that need to be made before testing). Do not invent figures. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Amaç: bir arıza sınaması tasarlamak.**

```text
Help me design a controlled failure test for [service].

What I want to learn: [for example whether availability holds if one database node fails].
Environment for the test: [describe, e.g. a production-like test environment].
Safeguards available: [monitoring, rollback, people on hand].

Describe a step-by-step test plan: hypothesis, what to break and how, what to observe, who is present, what stops the test, and how to record what happened. Keep it away from production unless I say it is safe. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Yapay zeka becerileri

- [capacity-planning](../../../../skills/capacity-planning/SKILL.md): bir hizmetin zaman içinde ihtiyaç duyduğu kaynakları tahmin etmek ve bunları eklemek için bir strateji seçmek için kullanın.
- [demand-forecasting](../../../../skills/demand-forecasting/SKILL.md): gelecekteki yükü geçmiş verilerden ve iş planlarından bir aralık olarak tahmin etmek için kullanın.
- [load-testing](../../../../skills/load-testing/SKILL.md): bir zirveden önce gerçekçi talep uygulayan sınamalar tasarlamak için kullanın.
- [performance-testing](../../../../skills/performance-testing/SKILL.md): teslimatın parçası olarak kritik yollarda hızı ve kaynak kullanımını denetlemek için kullanın.
- [chaos-testing](../../../../skills/chaos-testing/SKILL.md): bileşenler arızalandığında erişilebilirliğin korunup korunmadığını sınamak için kullanın.

## Temel kaynaklar

- **Embracing Risk** (*Site Reliability Engineering*, Google, sre.google): erişilebilirliğin ekonomisi, istek tabanlı ölçüm ve hata bütçesi.
- **Capacity planning** (Wikipedia): tanımlar ile önde gitme, geriden gelme, eşleştirme ve uyarlama stratejileri.
- **Monitoring Distributed Systems** (*Site Reliability Engineering*, Google, sre.google): doygunluk dahil altın sinyaller.
- **High availability** (Wikipedia): sistemleri kesintisiz çalışma için tasarlama üzerine arka plan.

## Kaynakça

1. Embracing Risk — Google SRE book, sre.google — https://sre.google/sre-book/embracing-risk/
2. Capacity planning — Wikipedia — https://en.wikipedia.org/wiki/Capacity_planning
3. Monitoring Distributed Systems — Google SRE book, sre.google — https://sre.google/sre-book/monitoring-distributed-systems/
4. Service Level Objectives — Google SRE book, sre.google — https://sre.google/sre-book/service-level-objectives/
5. High availability — Wikipedia — https://en.wikipedia.org/wiki/High_availability
6. Scalability — Wikipedia — https://en.wikipedia.org/wiki/Scalability
7. Load testing — Wikipedia — https://en.wikipedia.org/wiki/Load_testing
8. Chaos engineering — Wikipedia — https://en.wikipedia.org/wiki/Chaos_engineering
9. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
