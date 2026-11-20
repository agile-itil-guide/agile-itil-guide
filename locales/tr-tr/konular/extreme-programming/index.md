# Extreme Programming

**Extreme Programming (XP), mühendislik uygulaması konusunda en belirgin olan çevik yöntemdir; önce test etme, sürekli entegre etme ve kodun sahipliğini paylaşma alışkanlıkları, canlı bir hizmette sık değişikliği güvenli kılan şeydir.**

## Bu neden önemli

Sık değişiklik, sürekli teslimin amacı ve hizmet yönetiminin kaygısıdır. İkisini uzlaştırmanın yolu daha fazla onay toplantısı değil, bir değişikliğin kullanıcılara ulaşmadan önce çalıştığını bilme yeteneğinin güçlenmesidir. Extreme Programming, bu yeteneğin nasıl kurulacağı konusunda en çok şey söyleyen çevik yöntemdir: önce testleri yazın, günde birkaç kez entegre edin, tasarımı basit tutun ve kodun sorumluluğunu paylaşın.

Birçok ekip Scrum'ın etkinliklerini ve panolarını alır, mühendislik uygulamalarını geride bırakır. Sonuç, sprintlerle planlayan ama korkuyla sürüm çıkaran bir ekiptir. XP'nin uygulamaları eksik yarıdır. Sonucu işletmek zorunda olan herkes için önemlidir; çünkü otomatik testlerle, küçük sürümlerle ve paylaşılan bilgiyle geliştirilmiş bir hizmeti desteklemek, birkaç kişinin büyük, sınanmamış yığınlar halinde geliştirdiği bir hizmeti desteklemekten daha kolaydır.

XP ayrıca kuruluştan kolayca gözden kaçan bir şey ister: sürdürülebilir bir tempo, gereken tüm becerilere sahip bütün bir ekip ve gerçekten ulaşılabilir bir müşteri. Bunlar yalnızca programcıların alışkanlıkları değil, çalışma ortamının koşullarıdır. Bu konu yöntemi, sınırlarına ilişkin kanıtı ve uygulamalarının değişiklik sağlama, sürüm yönetimi ve bilgi yönetimi gibi ITIL uygulamalarına nasıl bağlandığını açıklar.

## Temel kavramlar

### XP nereden geldi

Kent Beck, XP'yi bir bordro projesi olan Chrysler Comprehensive Compensation System (C3) üzerinde çalışırken geliştirdi. [Extreme programming hakkındaki Wikipedia maddesine](https://en.wikipedia.org/wiki/Extreme_programming) göre Beck, Mart 1996'da proje lideri oldu ve yöntemi orada geliştirdi; Ward Cunningham önemli bir etki, Ron Jeffries ise ekibe koçluk yapmak üzere katıldı. Kitabı *Extreme Programming Explained* Ekim 1999'da çıktı. Chrysler, Daimler-Benz şirketi satın aldıktan sonra Şubat 2000'de C3 projesini iptal etti.

Madde, birçok XP uygulamasının yeni olmadığına dikkat çeker. 1960'ların başında NASA'nın Mercury Projesi'nde önce test etme yaklaşımından söz eder. XP'nin hamlesi iyi uygulamaları "aşırı" düzeylere taşımaktı: test etmek iyiyse sürekli test edin; gözden geçirmek iyiyse çiftler halinde çalışarak sürekli gözden geçirin. Beck ve Cunningham, Çevik Manifesto'yu yazan 17 kişi arasındaydı (bkz. Konu 1.1 — Çevik Manifesto).

### Beş değer

XP beş değer belirtir:

| Değer | Ne anlama gelir | Hizmet işinde |
|---|---|---|
| **İletişim** | Geliştiriciler, kullanıcılar ve müşteriler arasında, çoğunlukla konuşarak ve tasarımları basit tutarak ortak anlayış kurmak | Geliştiriciler ve operasyon çalışanları bir sürümün yayımlanmadan önce nasıl davranacağını konuşur |
| **Sadelik** | İşe yarayan en basit şeyi yapın ve spekülatif gelecekteki ihtiyaçlar için inşa etmeyin | İzlenecek, güvenceye alınacak ve açıklanacak daha az hareketli parça |
| **Geri bildirim** | Testlerden, müşterilerden ve ekibin kendi tahminlerinden hızla öğrenmek | Hızlı test sonuçları ve üretim izlemesi öğrenme süresini kısaltır |
| **Cesaret** | Yeniden düzenlemek, eskimiş kodu atmak ve zor sorunlarda sebat etmek | Kimsenin dokunmaya cesaret edemediği eski bir bileşeni emekliye ayırmak |
| **Saygı** | Takım arkadaşlarına ve kişinin kendi işine saygı | Arızalardan sonra suçlamasız gözden geçirme ve adil nöbet yükü |

Madde, saygının *Extreme Programming Explained*'in ikinci baskısında, ilk dört değerden sonra eklendiğini not eder.

### Uygulamalar

XP uygulamaları hakkındaki madde, on iki uygulamayı dört kümede gruplar. En iyi, kendini destekleyen bir sistem olarak anlaşılırlar.

| Grup | Uygulamalar | Amaç |
|---|---|---|
| **İnce ölçekli geri bildirim** | Eşli programlama, planlama oyunu, test güdümlü geliştirme, bütün ekip | Geri bildirimi aylar değil, dakikalar ya da günler içinde almak |
| **Sürekli süreç** | Sürekli entegrasyon, tasarım iyileştirme (refactoring), küçük sürümler | Yazılımı her zaman yayımlanabilir durumda tutmak |
| **Ortak anlayış** | Kodlama standardı, ortak kod sahipliği, basit tasarım, sistem metaforu | Ekipteki herkesin sistemin herhangi bir parçasını güvenle değiştirebilmesini sağlamak |
| **Programcı refahı** | Sürdürülebilir tempo | İnsanları yıllarca dinlenmiş ve etkili tutmak |

Başlıca olanların kısa bir tanımı:

- **Eşli programlama (pair programming):** iki kişi tek bir iş istasyonunda tek bir görev üzerinde çalışır; biri yazar, biri gözden geçirir ve sık sık eş değiştirirler.
- **Test güdümlü geliştirme (TDD):** programcı önce başarısız olan bir test yazar, sonra onu geçirecek kadar kod yazar.
- **Sürekli entegrasyon (CI):** geliştiriciler işlerini birkaç saatte bir ortak depoya birleştirir; böylece entegrasyon sorunları erken ortaya çıkar.
- **Küçük sürümler:** müşterilerin ilerlemeyi görüp yanıt verebilmesi için çalışan yazılımı sık, küçük adımlarla teslim edin.
- **Ortak kod sahipliği:** ekipteki herkes kodun herhangi bir parçasını değiştirebilir.
- **Sürdürülebilir tempo:** düzenli fazla mesaiden kaçının ve art arda iki hafta fazla mesaiye asla izin vermeyin.

### Tartışmalar ve sınırlar

Madde birkaç eleştiriyi kaydeder. Matt Stephens ve Doug Rosenberg, 2003 tarihli bir kitapta, XP'nin uygulamalarının birbirine bağlı olduğunu, bu yüzden yalnızca bazılarını benimsemenin süreci zayıflattığını savundu. Eleştirmenler ayrıca eşli programlamanın normal çalışma biçimi olmasını, büyük önceden tasarımın olmayışını, tek hata noktası olarak sahada müşteriyi ve gayriresmî değişiklik taleplerinin yeniden işe ve kapsam kaymasına yol açmasını sorguladı. P. McBreen ile Boehm ve Turner da eleştirel değerlendirmeler yazdı. Madde, çevik uygulayıcıların bu eleştirilerin çoğunu yanlış anlama olarak gördüğünü ekler.

Ölçek konusunda madde, 2004'te tanıtılan Industrial XP'nin XP'yi 23 uygulamayla daha büyük ve dağıtık ekiplere genişlettiğini söyler. Ayrıca atıf gerektirdiği işaretlenmiş bir iddiayı bildirir: ThoughtWorks'ün altmış kişiye kadar dağıtık XP projelerinde makul başarı elde ettiği. Bu iddiayı dikkatle okuyun ve daha geniş tartışma için Konu 1.8 — Çevikliği Ölçeklendirme'ye bakın.

Madde, sürekli entegrasyon ve küçük sürümlerin ötesinde dağıtım ya da üretim izlemesini ele almaz. XP, yazılımı işletme hakkında az şey söyler. Bunu hizmet yönetiminden getirirsiniz ve devir teslimi daha az riskli hale getirmek için XP'yi kullanırsınız.

### XP ve ITIL'in değişikliğe bakışı

ITIL'in değişiklik sağlama uygulaması (bkz. Konu 3.4 — Değişiklik Sağlama), risk denetim altında tutulsun diye değişikliklerin değerlendirilmesi, yetkilendirilmesi ve zamanlanmasıyla ilgilenir. XP riski farklı bir yerde denetler: kodun içinde, testler, küçük adımlar ve paylaşılan bilgi yoluyla. Küçük, otomatik olarak test edilen, entegre edilen ve geri alması kolay bir değişiklik, makul herhangi bir değerlendirmeyle daha düşük riskli bir değişikliktir. XP uygulamalarından gelen kanıt değişiklik kararında kullanıldığında iki bakış birbirine uyar.

## İyi uygulamalar

1. **Uygulamaları bir bütün olarak benimseyin.** Eleştirmenlerin XP'nin uygulamalarının birbirini desteklediği noktası yararlı bir uyarıdır. Entegrasyonsuz test ya da küçük adımsız entegrasyon, toplamdan azını verir. Mümkün olduğunda onları birlikte tanıtın ve hangilerinin diğerlerine bağlı olduğunu öğrenin.
2. **Önemli değişiklikler için önce testi yazın.** Yeni bir davranış ya da hata düzeltmesi için sorunu gösteren başarısız bir test yazın, sonra düzeltin. Test, sorunun geri dönmesine karşı bir koruma olarak kalır; bu, özellikle olaylara yol açan arızalar için yararlıdır.
3. **Günde birkaç kez entegre edin.** Dalları kısa ömürlü tutun ve her birleştirmede otomatik olarak derleyip test edin. Bozuk bir derleme ekibin ilk önceliğidir.
4. **Küçük adımlarla sürüm çıkarın.** Her küçük sürüm daha az risk taşır ve anlaması ve geri alması daha kolaydır. Boru hattınızın güvenle destekleyebileceği en küçük aralığı hedefleyin ve güven arttıkça kısaltın.
5. **Sürekli yeniden düzenleyin.** Tasarımı bir yeniden yazım için saklamak yerine her gün biraz iyileştirin. Bunu güvenli kılan test paketidir.
6. **Tasarımı olabildiğince basit tutun.** Şimdi gerekeni inşa edin ve kullanılmayanı kaldırın. Daha küçük bir sistemin izlenecek, yamalanacak ve açıklanacak daha az şeyi vardır.
7. **Kodun sahipliğini paylaşın.** Herhangi bir ekip üyesinin, testler ve ortak standartlarla desteklenerek herhangi bir parçayı değiştirmesine izin verin. Bu, birkaç uzmana bağımlılığı azaltır; ki bu da hizmet için bir erişilebilirlik riskidir.
8. **Riskli ya da tanıdık olmayan işte eşli çalışın.** Eşliği zor değişiklikler, ekibe uyum ve nöbet gölgelemesi için kullanın. Onu bilgiyi yayan ve hataları yakalayan bir araç olarak ele alın ve her görev için bir kural yapmayın.
9. **Sürdürülebilir bir tempo tutun.** İşi, fazla mesai nadir olacak ve haftalarca tekrarlanmayacak şekilde planlayın. Yorgun bir nöbetçi mühendis bir hizmet riskidir (tempo hakkında bkz. Konu 1.2 — Çevik İlkeler).
10. **Müşteriyi ekibin parçası yapın.** İş sırasında soruları yanıtlayabilecek gerçek bir kullanıcı ya da kullanıcı temsilcisi bulun. Tek bir kişinin tek hata noktası olduğu eleştirisini hatırlayın; bu yüzden birden fazla ses dahil edin.
11. **Kabul ölçütlerini mümkün olduğunda test olarak yazın.** Müşterinin beklentilerini her derlemede çalışan otomatik kontrollere dönüştürün. Böylece davranışı hem belgelerler hem korurlar.
12. **Testlere operasyonel kontrolleri dahil edin.** İzleme, günlükleme ve kurtarma davranışı için kontrolleri boru hattına ekleyin; böylece operasyonel hazırlık her değişiklikte doğrulanır (bkz. Konu 3.5 — Sürüm ve Dağıtım Yönetimi).

## Ekibinizle tartışılacak sorular

**Bir değişikliğin kullanıcılara ulaşmadan önce çalıştığını nasıl biliyoruz ve bilmek ne kadar sürüyor?**

Bir değişikliğin bir geliştiricinin dizüstü bilgisayarı ile üretim arasında geçtiği kontrolleri izleyin. Kaçının otomatik olduğunu ve her birinin ne kadar sürdüğünü sayın. Tipik yanıtlar bir elle test, bir gözden geçirme ve bir umuttur. Hangi kontrolün en çok sorunu yakaladığını ve hangisinin hiçbir şey yakalamadığını sorun. Otomatikleştirilecek bir elle kontrol seçerek devam edin.

**Sistemimizin hangi parçalarını kim değiştirebilir ve bu kişiler yokken ne olur?**

Bileşenleri ve her birini anlayan kişileri listeleyin. Arkasında tek bir kişi olan bileşenler hizmet için risklerdir. Ortak sahiplik XP'nin yanıtıdır ve güvenli olması için testlere ve ortak standartlara ihtiyaç duyar. Bir kişinin bir ay içinde başka birine neyi öğretebileceğini sorun. Kolaylaştırıcı, tatillerin ya da hastalığın bir düzeltmeyi hiç geciktirip geciktirmediğini sorabilir.

**Eşli çalışma bize en çok nerede yardımcı olur ve nerede yalnızca yavaşlatır?**

Eşli programlama tartışmalıdır; bu yüzden dürüst görüşlere davet edin. İnsanlara yaptıkları en iyi ve en kötü eşli çalışmayı sorun. Eşli çalışma çoğunlukla tanıdık olmayan sistemlerde, zor değişikliklerde ve ekibe uyumda yardımcı olur. Bir kişinin iyi yapabileceği rutin işte daha az yardımcı olur. Eşli çalışmayı bir ay boyunca deneyeceğiniz bir durum ve onu nasıl yargılayacağınız konusunda anlaşın.

**Baskı altında kalitemize ne oluyor ve önce neyi bırakıyoruz?**

Yakın tarihli bir sıkışmayı ve neyin atlandığını sorun: testler, gözden geçirmeler, dokümantasyon. Sonrasında ne olduğunu sorun. Çoğunlukla atlanan iş olaylar olarak geri döndü. Mesele kalıbı fark etmek ve hangi uygulamaların korunacağına önceden karar vermektir. Suçlamadan kaçının ve yanıtı sürdürülebilir tempoya bağlayın.

**İşimizi ne sıklıkla birleştiriyoruz ve bizi ne bekletiyor?**

Tipik bir dalın ne kadar yaşadığını ve onu neyin geciktirdiğini sorun. Uzun dallar genellikle büyük değişiklikleri, yavaş gözden geçirmeleri ya da güvenilmez bir derlemeyi yansıtır. Her biri farklı bir çözümdür. Birleştirmeyi birkaç saatte yapmanın normal durum olması için ekibin ne yapabileceğini sorun. Kaldırılacak bir engel seçin.

**Ekibin ulaşabildiği bir müşterimiz ya da kullanıcımız var mı, yoksa ne istediklerini tahmin mi ediyoruz?**

Kullanıcıların neye ihtiyaç duyduğuna ilişkin soruları kimin yanıtladığını ve ne kadar sürdüğünü sorun. Yanıt uzun bir zincirse, hangi sorunun yanlış anlaşılmasının en maliyetli olduğunu sorun. XP'nin kendi eleştirmenlerini hatırlayın: tek bir müşteri temsilcisi bir darboğaz olabilir. Birkaç kullanıcıya kısa ve sık nasıl ulaşılacağını tartışın.

## Uygulamada: çevik bir ITIL örneği

Bir kamu toplu taşıma kurumunun dokuz kişilik dijital ekibi, yolculuk planlama uygulamasını ve şehirdeki diğer geliştiricilerin kullandığı canlı varış verisi akışını geliştirir ve işletir. Ekip, dört günlük elle bir test döngüsünden sonra aylık sürüm çıkarıyor. Bir sürüm kötü gittiğinde geri almak yarım gün sürüyor; bu yüzden ekip daha sık sürüm çıkarmaya isteksiz. Aynı zamanda en deneyimli geliştirici olan operasyon lideri, akışın nasıl çalıştığını başka kimse bilmediği için mesai dışı çağrıların çoğunu yanıtlıyor.

Ekip birkaç XP uygulamasını birlikte benimsemeye karar verir. Her birleştirmede derleyen ve birim testlerini çalıştıran sürekli entegrasyon kurar. Üretimde bulunan her hata için, düzeltmeden önce başarısız bir test yazar. İki geliştirici, akış işinde günde bir saat operasyon lideriyle eşli çalışır. Ekip ayrıca önceki sürüme dakikalar içinde geri dönebilen bir dağıtım adımı ekler.

Dört ay sonra ekip her hafta sürüm çıkarıyor. Test paketi, elle döngünün ancak son gün bulacağı iki gerilemeyi sürümden önce yakalıyor. Üç geliştirici artık akış çağrılarının çoğunu ele alabiliyor. Her şey işlemiyor: test paketinin çalışması 25 dakika sürdüğü için geliştiriciler amaçlanandan daha seyrek birleştiriyor ve varış akışındaki hatalı bir değişiklik, testlerinin gerçek bir uç duruma uymayan örnek veri kullanması yüzünden gözden kaçıyor. Ekip yavaş testleri ikinci bir aşamaya taşır; böylece ilk sonuçlar beş dakika içinde gelir ve akışın çıktısına bir izleme kontrolü ekler. Ayrıca eşli çalışmanın her görev için bir kural değil, zor sorunlar ve ekibe uyum için bir araç olarak kalacağı konusunda anlaşırlar.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri XP'nin uygulamalarının sahibidir. Geri bildirimi en hızlı veren uygulamalarla başlayın: otomatik testler ve sürekli entegrasyon. Test paketinizi operasyonun da kullandığı bir ürün olarak ele alın. Hizmetin ne yapması gerektiğini anlatır ve yapmayı bıraktığında size hızla söyler.

### Hizmet ve operasyon ekipleri

Operasyon çalışanları XP fikirlerini kendi işleri için kullanabilir: çalışmadan önce test edilen altyapı ve yapılandırma değişiklikleri, sık entegre edilen küçük değişiklikler ve eşli çalışma ve ortak sahiplik yoluyla ekip içinde paylaşılan bilgi. Teslimat ekiplerinden üretimde gördüğünüz arızaları kapsayan testler isteyin ve nelerin test edileceğine yön vermek için olay geçmişini sunun.

### Liderlik ve yönetişim

Liderler tempoyu koruyarak, derleme ve test altyapısını finanse ederek ve kalitenin sonradan denetlenerek değil, işin içine inşa edildiğini kabul ederek XP'yi mümkün kılar. Boru hattından gelen güvenlik kanıtını, örneğin test sonuçlarını ve sürüm geçmişlerini isteyin ve yinelenen elle kanıt talep etmeyin.

### Müşteriler ve kullanıcılar

Müşterilerin XP'de en doğrudan rolü vardır: ekibin geri bildirim döngüsünün parçasıdırlar. Küçük sürümleri denemeniz, soruları çabuk yanıtlamanız ve bu hafta en çok neyin önemli olduğunu söylemeniz istenmesini bekleyin. Karşılığında daha az sürpriz ve bildirdiğiniz sorunlar için daha hızlı düzeltmeler görmelisiniz.

## Yaygın başarısızlık biçimleri

- **Yalnızca ritüelleri benimsemek.** Ekipler ayakta toplantıları ve panoları alır, testleri ve entegrasyonu atlar. Bunun yerine, en büyük getiriyi verdikleri için otomatik testler ve sürekli entegrasyonla başlayın.
- **Eşli çalışmayı bir kural olarak görmek.** Tüm işte zorunlu eşli çalışma insanları bunaltır ve rutin görevleri yavaşlatır. Bunun yerine, eşli çalışmayı zor sorunlar, ekibe uyum ve bilgi aktarımı için kullanın ve nasıl işlediğini gözden geçirin.
- **Kimsenin güvenmediği bir test paketi.** Yavaş ya da güvenilmez testler göz ardı edilir. Bunun yerine, paketi hızlı tutun ve kararsız (flaky) testleri çabucak düzeltin ya da silin.
- **Standartsız ortak sahiplik.** Herkes her şeyi değiştirebilir ve kod çürür. Bunun yerine, onu ortak kodlama standartları, gözden geçirme ve otomatik kontrollerle eşleştirin.
- **Tek bir müşteri temsilcisi.** Bir kişi darboğaz ya da yanlılık kaynağı olur. Bunun yerine, teması birkaç kullanıcıya yayın ve kararları gerçek kullanımla denetleyin.
- **Tasarımı tümüyle atlamak.** Ekipler bir yön olmadan tekrar tekrar yeniden düzenler. Bunun yerine, mimarinin hafif bir resmini tutun ve düzenli aralıklarla gözden geçirin.
- **Fazla mesainin normal olması.** Uzun saatler kaliteyi aşındırır ve olaylara yol açar. Bunun yerine, sürdürülebilir bir tempoya göre planlayın ve tekrarlanan fazla mesaiyi kapsamı azaltma işareti olarak görün.
- **Operasyonu göz ardı etmek.** XP, yazılımı işletme hakkında az şey söyler ve ekipler bunun kapsandığını varsayar. Bunun yerine, testlere operasyonel kontroller ekleyin ve operasyon çalışanlarını planlamaya davet edin.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Test | Test elle yapılır ve geçtir | Bazı ekiplerin otomatik birim testleri vardır | Ekipler testleri kodla birlikte yazar ve her değişiklikte çalıştırır | Test sonuçları ve kaçan kusurlar izlenir ve gözden geçirilir | Test stratejisi hizmetler arasında eşgüdümlenir ve operasyonla paylaşılır |
| Entegrasyon ve sürüm | Entegrasyon seyrek, sürümler büyüktür | Bazı ekipler sürekli entegrasyon kullanır | Ortak bir boru hattı her değişikliği derler, test eder ve dağıtır | Sürüm sıklığı ve hata oranı ölçülür ve iyileştirilir | Boru hatları ekipler ve tedarikçiler arasında eşgüdümlenir |
| Ortak sahiplik ve bilgi | Bilgi birkaç bireyde durur | Bazı ekipler eşli çalışır ya da işi döndürür | Standartlarla ortak sahiplik norm haline gelir | Bilgi boşlukları izlenir ve azaltılır | Bilgi ekipler arasında ve çalışma kılavuzlarına serbestçe akar |
| Tempo ve refah | Fazla mesai rutindir | Bazı ekipler iş yüklerini izler | Sürdürülebilir tempo belirtilmiş bir politikadır | Nöbet yükü ve fazla mesai ölçülür ve gözden geçirilir | İş yükü ortak verilere dayanarak ekipler arasında dengelenir |

## Kontrol listesi

- [ ] Ekip hangi XP uygulamalarını kullanacağı konusunda anlaştı ve onları birlikte denedi.
- [ ] Otomatik testler her değişiklikte çalışıyor ve başarısız bir derleme ilk önce düzeltiliyor.
- [ ] Her üretim hatası için, onu yakalamış olacak bir test yazılıyor.
- [ ] İş ortak dala günde birkaç kez birleştiriliyor.
- [ ] Sürümler küçük ve geri alma hızlı yapılabiliyor.
- [ ] Sistemin her bir parçasını birden fazla kişi değiştirebiliyor ve destekleyebiliyor.
- [ ] Eşli çalışma zor sorunlar ve ekibe uyum için kullanılıyor ve etkisi gözden geçiriliyor.
- [ ] Fazla mesai nadir ve haftalarca tekrarlanmıyor.
- [ ] İş sırasında soruları yanıtlamak için bir kullanıcı ya da kullanıcı temsilcisi ulaşılabilir durumda.
- [ ] Testler, izleme ve kurtarma davranışı için kontrolleri içeriyor.

## Yapay zeka istemleri

**Amaç: bir üretim olayını bir teste ve bir ders listesine dönüştürmek.**

```text
Help me learn from a production incident using Extreme Programming habits.

Incident description (factual, blameless, in order): [paste what happened, how it was detected, and how it was fixed].
The part of the system involved: [describe the component and what it does].
Our current tests for that part: [describe what is tested today, or write "unknown"].

Propose: (1) a test, described in plain words, that would have caught this before release; (2) two other tests worth adding nearby; (3) one change to our release process to make a similar fault less likely. Do not invent details about our system. Ask clarifying questions first if the description is too thin, mark assumptions, and list what you are unsure of.
```

**Amaç: ekibinizin küçük değişiklikleri ne kadar güvenle yayımlayabildiğini değerlendirmek.**

```text
I want to understand how safe it is for our team to release small changes often.

Our path from change to production, step by step: [paste the steps, who does each, and roughly how long each takes].
Our automated checks: [list tests, builds, and scans, or write "none"].
How we roll back: [describe].
The last two releases that went wrong: [paste short factual descriptions].

Identify the steps that rely on manual work or one person's knowledge. For each, suggest one small automation or sharing step. Do not claim any standard requires something unless I pasted its text. Separate what the text shows from what you assume, and list what you are unsure of.
```

**Amaç: eşli çalışmayla bir aylık bir deney tasarlamak.**

```text
Help me design a one-month experiment with pair programming for a team of [number] people working on [type of system].

Our reasons for trying it: [for example "reduce single points of failure on the feed service"].
Constraints: [for example remote working, on-call duties, mixed experience levels].

Propose which kinds of work to pair on and which to leave alone, how to rotate partners, what to observe (use observations such as questions answered and defects found, and do not invent numbers), and how the team will decide at the end whether to continue. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Amaç: operasyonel hazırlık için bir Bitti Tanımı'nı denetlemek.**

```text
Here is our current Definition of Done: [paste it].
Things the operations or support team has asked for: [paste, or write "unknown"].

Compare the two. List items operations would need that are missing, and for each one say whether it could be checked automatically in a build pipeline, and how. Do not state that any standard requires an item unless I have pasted its text. Mark assumptions and list what you are unsure of.
```

## Yapay zeka becerileri

- [extreme-programming](../../../../skills/extreme-programming/SKILL.md): eşli çalışma, test güdümlü geliştirme ve sürekli entegrasyon gibi XP uygulamalarını gözden geçirmek ya da tanıtmak için kullanın.
- [user-story](../../../../skills/user-story/SKILL.md): müşteri ihtiyaçlarını, otomatik testlere dönüşebilecek kabul ölçütleriyle hikâyelere dönüştürmek için kullanın.
- [agile-delivery](../../../../skills/agile-delivery/SKILL.md): küçük, sık sürümleri ve onları güvenli kılan kontrolleri planlamak için kullanın.
- [agile-reflection](../../../../skills/agile-reflection/SKILL.md): uygulamaların ne kadar iyi işlediğini gözden geçirmek ve bir değişiklik seçmek için kullanın.
- [runbook](../../../../skills/runbook/SKILL.md): tek bir kişinin elindeki bilgiyi ortak, sınanmış bir prosedüre dönüştürmek için kullanın.

## Temel kaynaklar

- **Extreme programming** ve **Extreme programming practices** (Wikipedia): atıflarla birlikte tarihçeye, değerlere, uygulamalara ve eleştiriye genel bakış.
- **Extreme Programming Explained** (Kent Beck): yöntemin özgün ifadesi; ikinci baskısı saygı değerini ekler.
- **Manifesto for Agile Software Development** (agilemanifesto.org): XP, yazarları Manifesto'yu yazan yöntemlerden biridir.
- **Extreme Programming Refactored: The Case Against XP** (Matt Stephens ve Doug Rosenberg, 2003): en bilinen eleştiri; kendi varsayımlarınızı sınamak için yararlı.

## Kaynakça

1. Extreme programming — Wikipedia — https://en.wikipedia.org/wiki/Extreme_programming
2. Extreme programming practices — Wikipedia — https://en.wikipedia.org/wiki/Extreme_programming_practices
3. Pair programming — Wikipedia — https://en.wikipedia.org/wiki/Pair_programming
4. Test-driven development — Wikipedia — https://en.wikipedia.org/wiki/Test-driven_development
5. Continuous integration — Wikipedia — https://en.wikipedia.org/wiki/Continuous_integration
6. Code refactoring — Wikipedia — https://en.wikipedia.org/wiki/Code_refactoring
7. Kent Beck — Wikipedia — https://en.wikipedia.org/wiki/Kent_Beck
8. Ward Cunningham — Wikipedia — https://en.wikipedia.org/wiki/Ward_Cunningham
9. Manifesto for Agile Software Development — Beck et al., agilemanifesto.org — https://agilemanifesto.org/
