# Bilgi Güvenliği Yönetimi

**Bilgi güvenliği yönetimi, bilginin gizliliğini, bütünlüğünü ve erişilebilirliğini risk tabanlı denetimlerle korur; çevik bir kuruluşta denetimler, sonda eklenen bir kapı olarak değil, teslimat hattına ve ekiplerin günlük alışkanlıklarına yerleştirildiğinde en iyi işler.**

## Bu neden önemli

Her hizmet, birinin önemsediği bilgiyi tutar: müşterilerin bilgileri, ödeme kayıtları, sağlık verileri, iç planlar. Bir güvenlik arızası bilginin ilişkin olduğu insanlara zarar verir, kuruluşun itibarını zedeler ve hukuki ve mali yaptırımlar getirebilir. Hizmet yönetimi ekipleri çoğu zaman arızayı bir olay olarak ilk gören ve sonrasında normal işleyişi geri getirmesi gerekenlerdir.

Güvenlik ve sürekli teslimat çoğunlukla zıt olarak sunulur: güvenlik yavaşla der, teslimat hızlan der. Bu görüş yararsızdır. Yalnızca bir sürümün sonunda gelen güvenlik, geç sürprizler ve aceleyle verilmiş istisnalar üretir. İşe yerleştirilmiş, otomatik çalışan denetimleri ve erken tartışılan riskleri olan güvenlik, hizmeti durdurmadan korur. Aynısı hizmet yönetimi için de geçerlidir: değişikliği güvenli kılan uygulamalar güvenlik değişikliklerini de güvenli kılar.

Bu konu, ana kaynakları olarak [bilgi güvenliğine ilişkin Wikipedia maddesini](https://en.wikipedia.org/wiki/Information_security) ve [ISO/IEC 27001 maddesini](https://en.wikipedia.org/wiki/ISO/IEC_27001) kullanır. İkisi de geneldir. İlki uzun bir maddedir ve bu rehber yaklaşık 243.000 karakterinin yalnızca ilk 100.000'ini okumuştur. Bu konu hukuki tavsiye vermez; yasalar, düzenlemeler ve sözleşmesel yükümlülükler ülkeye ve sektöre göre farklılık gösterir ve doğru kaynak sizin için geçerli olan kuralın metnidir.

## Temel kavramlar

### Bilgi güvenliği nedir

Wikipedia bilgi güvenliğini, bilgi risklerini azaltarak bilgiyi korumak; bilginin yetkisiz erişimini, kullanımını, ifşasını, kesintiye uğramasını, silinmesini, bozulmasını, değiştirilmesini ya da değer kaybını önlemeyi ya da azaltmayı ve olayların etkisini azaltmayı amaçlamak olarak tanımlar. Elektronik, fiziksel ve soyut bilgiye uygulanır ve bilgi riski yönetiminin bir parçasıdır.

### CIA üçlüsü

Temel hedefler, politika verimliliği ve kurumsal üretkenlikle dengelenen **gizlilik (confidentiality)**, **bütünlük (integrity)** ve **erişilebilirliktir (availability)**. Madde bunları şöyle betimler:

| Hedef | Anlamı | Bir hizmetteki örnek |
|---|---|---|
| **Gizlilik** | Bilgi yetkisiz ifşadan korunur | Hasta kayıtlarını yalnızca yetkili personel görebilir |
| **Bütünlük** | Bilgi doğru ve eksiksizdir ve yetkisiz ya da fark edilmeyen bir biçimde değiştirilemez | Bir ödeme tutarı iz bırakmadan değiştirilemez |
| **Erişilebilirlik** | Bilgiye ihtiyaç duyulduğunda erişilebilir | Hizmet ayakta kalır ve hizmet reddi saldırılarına direnir |

Madde, gizliliğin, daha geniş bir kavram olarak nitelediği mahremiyetten (privacy) farklı olduğunu not eder. Ayrıca kuruluşların özgünlük, hesap verebilirlik, inkâr edilemezlik ve güvenilirlik gibi hedefler ekleyebileceğini ve genişletilmiş bir model olan Parkerian Hexad'ın tartışmalı değerleri olduğunu not eder. Erişilebilirlik doğrudan hizmet yönetimine bağlanır (bkz. Konu 3.11 — Erişilebilirlik, Kapasite ve Performans).

### Risk yönetimi

Madde riski, bir bilgi varlığına zarar verme olasılığı olarak betimler. **Zayıflıklar (vulnerabilities)** eksikliklerdir, **tehditler (threats)** olası zarar nedenleridir ve **etki (impact)** ortaya çıkan kayıptır. Risk yönetimi, yönetimin bir riski kabul edebileceği, azaltabileceği, devredebileceği (örneğin sigortayla) ya da kaçınabileceği, sürekli ve yinelemeli bir süreçtir. Geriye kalana **artık risk (residual risk)** denir. Madde altı adım sayar: varlıkları belirlemek, tehditleri değerlendirmek, zayıflıkları değerlendirmek, etkiyi hesaplamak, denetimleri seçip uygulamak ve bu denetimleri değerlendirmek.

### Denetimler ve derinlemesine savunma

Denetimler gizliliği, bütünlüğü ya da erişilebilirliği korur. Madde, birbiriyle örtüşen denetimlerin katmanlanması olan **derinlemesine savunmayı (defense in depth)** betimler; denetim türleri yönetsel (politikalar, yordamlar), mantıksal (erişim denetimi ve şifreleme gibi teknik önlemler) ve fiziksel (kilitler, tesisler) olarak betimlenir. Hiçbir tek denetim yeterli değildir; katmanlar birbirlerinin arızalarını örter.

### Güvenlik olayları

Madde, bilgisayar güvenliği olay yönetimini güvenlik etkinliklerini izleme, algılama ve bunlara yanıt verme olarak betimler; ihlaller algılandığında devreye alınan olay müdahale planları tipik olarak bir olay müdahale ekibi tarafından yürütülür. Güvenlik olayları bir olay türüdür ve aynı rollerden, iletişimden ve suçlamasız öğrenmeden (bkz. Konu 3.2 — Olay Yönetimi) ve ayrıca delilleri korumak ve gerekli olduğunda düzenleyicilere ya da etkilenen kişilere bildirimde bulunmak gibi özel adımlardan yararlanır.

### ISO/IEC 27001 ve 27002

Wikipedia'ya göre **ISO/IEC 27001**, bilgi güvenliği risklerini değerlendirme ve ele alma dahil bir bilgi güvenliği yönetim sistemini (ISMS) kurma, uygulama, sürdürme ve sürekli iyileştirme şartlarını ortaya koyar. Şartları geneldir ve her türden, büyüklükten ya da nitelikteki kuruluş için tasarlanmıştır. İlk sürüm, BS 7799-2 İngiliz standardından Ekim 2005'te, ikincisi 2013'te ve üçüncüsü ISO/IEC 27002:2022 ile uyumlu olarak Ekim 2022'de çıkmıştır; Şubat 2024'teki bir değişiklik iklim değişikliği düşüncesini eklemiştir.

Maddeden kilit olgular:

- ISMS şartları 4 ila 10. maddelerdedir: bağlam, liderlik, planlama, destek, operasyon, performans değerlendirmesi ve iyileştirme.
- 2022 sürümünün Ek A'sında dört temada 93 referans denetim vardır: kurumsal, insan, fiziksel ve teknolojik. 2013 sürümü 114 listelemişti. Ek A bir referans kümesidir, zorunlu bir kontrol listesi değildir: kuruluşlar hangi denetimleri dahil edip hariç tuttuklarını gerekçelendiren bir **Uygulanabilirlik Bildirimi (Statement of Applicability)** hazırlar.
- Bir yasa, sözleşme ya da şema gerektirmedikçe belgelendirme isteğe bağlıdır. ISO kuruluşları belgelendirmez; bağımsız belgelendirme kuruluşları bunu aşamalar halinde yapar, ardından gözetim denetimleri ve üç yıllık bir döngüyle yeniden belgelendirme gelir. Bir belge yalnızca belirtilen kapsamı içinde geçerlidir.
- **ISO/IEC 27002**, Ek A denetimleri hakkında rehberlik sağlar. Bir rehberdir ve buna karşı belgelendirme yapılamaz.

Madde, 2021 tarihli bir literatür taramasının belgelendirme sonuçları üzerine çok az ampirik çalışma bulduğunu not eder. Bir belge bir yönetim sisteminin var olduğunu gösterir; belirli bir ihlalin olamayacağının kanıtı değildir.

### Diğer çerçeveler ve yasalar

Bilgi güvenliği maddesi, NIST Siber Güvenlik Çerçevesi, Birleşik Krallık'taki Cyber Essentials, Avustralya'daki Essential Eight ve ödeme kartı endüstrisi standardı gibi birçok başka standardı ve şemayı adlandırır. Ayrıca Birleşik Krallık'ın Computer Misuse Act (1990) ve Data Protection Act (1998) yasalarını ve Amerika Birleşik Devletleri'nin HIPAA (1996), Gramm–Leach–Bliley Act (1999) ve Sarbanes–Oxley Act (2002) yasalarını da sıralar. Liste kuralların ne kadar çeşitli olduğunu gösterir. Hangilerinin sizin için geçerli olduğu nerede faaliyet gösterdiğinize, sektöre ve elinizde tuttuğunuz verilere bağlıdır; hukuk ya da uyum işlevinize sorun (bkz. Konu 5.7 — Yönetişim, Risk ve Uyum).

### Teslimat hattında güvenlik

Sürekli teslimata uyan uygulamalar şunları içerir:

- **Erken tehdit tartışması:** planlamada bir özellikle neyin ters gidebileceğini ve onu kimin kötüye kullanmak isteyeceğini sorun.
- **Otomatik denetimler:** her değişiklikte kodu, bağımlılıkları ve yapılandırmayı sonuçlar ekip tarafından görülebilir biçimde taramak (bkz. Konu 3.4 — Değişiklik Sağlama).
- **En az ayrıcalık (least privilege):** insanlara ve sistemlere yalnızca ihtiyaç duydukları erişimi vermek.
- **Sır yönetimi:** kimlik bilgilerini koddan uzak tutmak ve döndürmek.
- **Güvenlik sınaması:** döngünün parçası olarak sızma sınamaları ve otomatik sınamalar (aşağıdaki güvenlik sınaması becerisine bakın).
- **Günlükleme ve izleme:** şüpheli etkinliği algılamak (bkz. Konu 3.10 — İzleme ve Etkinlik Yönetimi).

Bu rehberin başka yerlerinde atıf yapılan DORA'nın rehberliği, yaygın güvenliği sürekli teslimatı destekleyen uygulamalar arasında sayar (bkz. Konu 3.5 — Sürüm ve Dağıtım Yönetimi).

### Kültür ve insanlar

Bilgi güvenliği maddesi, Roer ve Petric (2017) tarafından belirlenen yedi kültür boyutu dahil güvenlik kültürü üzerine araştırmalardan söz eder. Model ne olursa olsun, nokta, birçok ihlalin insanlarla başlamasıdır: bir kimlik avı iletisi, bir hata, baskı altında bir kestirme. Eğitim, net bildirim yolları ve dürüst hatalara karşı suçlamasız bir tutum, güvenliği suçlamadan daha çok iyileştirir.

### Kaynakların sınırları

Wikipedia maddesi CIA üçlüsüne yönelik belirli eleştiriler bildirmez ve yalnızca kısmen okunmuştur. ISO/IEC 27001 maddesi ISO/IEC 20000 ile ya da planla-uygula-denetle-önlem al (PDCA) döngüsüyle ilişkiyi tartışmaz. Bu konu teknik yönergeler vermez; platformlarınız için uzman rehberliğini ve uyum iddia etmeniz gerekiyorsa standartların metnini kullanın.

## İyi uygulamalar

1. **Hangi bilgiyi nerede tuttuğunuzu bilin.** Başlıca bilgi türlerinin, her birinin sahibinin, nerede saklandığının ve ne kadar hassas olduğunun bir listesini yapın. Belirlemediğinizi koruyamazsınız.
2. **Risk değerlendirmelerini sade bir dille yapın.** Her önemli hizmet için gizlilik, bütünlük ve erişilebilirlik açısından neyin ters gidebileceğini, ne kadar olası olduğunu ve ne kadar kötü olacağını sorun. Her riski kabul etme, azaltma, devretme ya da kaçınma kararlarını kaydedin (bkz. Konu 5.7 — Yönetişim, Risk ve Uyum).
3. **Denetimlerinizi katmanlayın.** Bir arızanın yetmemesi için politikaları, teknik denetimleri ve fiziksel denetimleri birleştirin. En hassas bilginizi hangi katmanların koruduğunu gözden geçirin.
4. **Denetimleri teslimat hattına yerleştirin.** Her değişiklikte kod, bağımlılıklar ve yapılandırma üzerinde otomatik güvenlik denetimleri çalıştırın ve başarısız denetimleri görünür kılın. Sorunları değişiklik noktasında düzeltin.
5. **Varsayılan olarak en az ayrıcalık verin.** Erişimi role ve ihtiyaca göre verin, düzenli olarak gözden geçirin ve insanlar ayrıldığında ya da rol değiştirdiğinde hemen kaldırın (bkz. Konu 3.6 — Hizmet Talebi Yönetimi).
6. **Sırları doğru yönetin.** Kimlik bilgilerini kaynak kodundan uzak tutun, yönetilen bir kasada saklayın ve döndürün. Bir olaydan sonra bunları hızla döndürebildiğinizi sınayın.
7. **Güvenlik olaylarını olay olarak ele alın.** Diğer olaylarla aynı rolleri, iletişimi ve gözden geçirmeyi kullanın ve delil, sınırlama ve bildirim için adımlar ekleyin. Planı uygulayın.
8. **Bildirim yükümlülüklerinizi bilin.** Hukuk ya da uyum işlevinizden, bir ihlalden sonra hangi yasaların ya da sözleşmelerin yetkililere ya da etkilenen kişilere bildirimde bulunmanızı ve bunun ne kadar hızlı olması gerektiğini gerektirdiğini öğrenin. Bunu kaynak metni alıntılayarak olay planına yazın.
9. **Tedarikçileri dahil edin.** Kritik tedarikçilere bilginizi nasıl koruduklarını sorun ve beklentileri sözleşmelere koyun (bkz. Konu 3.14 — Tedarikçi Yönetimi).
10. **Eğitin ve konuşun.** Gerçek örneklere dayalı kısa, düzenli eğitim verin ve bir hatayı ya da şüpheli bir iletiyi suçlanmadan bildirmeyi kolaylaştırın.
11. **Standartları yapı kaynağı olarak kullanın.** ISO/IEC 27001'i benimsiyorsanız Ek A'yı bir referans kümesi olarak ele alın, gerekçeli bir Uygulanabilirlik Bildirimi yazın ve ISMS'yi hafif tutun. Zorunlu olmadıkça belgelendirme isteğe bağlıdır.
12. **Ramak kalalardan öğrenin.** Ramak kalaları ve düşük önemdeki etkinlikleri örüntüler açısından gözden geçirin ve bunları biriktirme listesine ve risk kaydına aktarın.

## Ekibinizle tartışılacak sorular

**Sızsa insanlara zarar verecek hangi bilgileri tutuyoruz ve bunlar nerede?**

Her kişiden ele aldığı en hassas veriyi ve nerede durduğunu söylemesini isteyin. Karşılaştırın. Sürprizler yaygındır: sınama ortamlarında kopyalar, ortak klasörlerde dışa aktarımlar, kişisel veri içeren günlükler. Kolaylaştırıcı hangi kopyanın en az korunduğunu sorabilir. Azaltmak ya da daha iyi korumak için birini seçin.

**Bir güvenlik riskini kabul etme kararını en son ne zaman verdik ve kim verdi?**

Bir örnek isteyin. Kabul edilen riskler çoğu zaman sessizce, gecikme yoluyla verilir. Kimin karar vermesi gerektiğini, hangi bilgiye ihtiyaç duyduğunu ve nerede kaydedildiğini tartışın. Maddenin riski ele alma yolları listesi (kabul, azaltma, devretme, kaçınma) yararlı bir çerçevedir. Bir sonraki kararı kaydetmek için basit bir yer üzerinde anlaşın.

**Her değişiklikte hangi güvenlik denetimleri otomatik çalışıyor ve neleri yok sayıyoruz?**

Teslimat hattındaki denetimleri ve sonuçları listeleyin. Hangi bulguların rutin olarak yok sayıldığını ve nedenini sorun. Yok sayılan bulgular genellikle gürültüyü, sahiplik eksikliğini ya da zaman eksikliğini gösterir. Hangilerinin düzeltileceğine, hangilerinin gerekçeyle bastırılacağına ve listenin sahibinin kim olduğuna karar verin.

**Kimin neye erişimi var ve bunu en son ne zaman gözden geçirdik?**

Hassas bir sistem seçin ve ona kimlerin ulaşabildiğini listeleyin. Kimin ihtiyaç duyduğuyla karşılaştırın. Erişim çoğu zaman birikmiştir. Biri ayrıldığında erişimin ne kadar çabuk kaldırıldığını sorun. Bir gözden geçirme tarihi ve bir sahip üzerinde anlaşın.

**Şüpheli bir ihlalin ilk saatinde ne yapardık?**

Adımları gözden geçirin: kime haber verilir, ne korunur, ne kapatılır, kim kiminle konuşur. Boşluklar genellikle yetki ve delil etrafında ortaya çıkar. Planın nerede olduğunu ve en son ne zaman kullanıldığını sorun. Bir masa başı tatbikat planlayın.

**Güvenlik ya da mahremiyetle ilgili hangi kurallar bizim için geçerli ve bunu nasıl biliyoruz?**

Bunu bilmekten kimin sorumlu olduğunu sorun. Yanıt "hukuk" ya da "kimse" ise, mühendisliğin gereksinimleri nasıl öğrendiğini sorun. Kurallar ülkeye ve sektöre göre farklıdır, bu yüzden faaliyet gösterdiğiniz yerleri listeleyin. Hukuk ya da uyum işlevinden kaynak metniyle birlikte kısa bir liste istemek üzere anlaşın.

## Uygulamada: çevik bir ITIL örneği

Bir üniversitenin araştırma bilişimi hizmeti, tıbbi çalışmalardan veri kümeleri tutuyor ve araştırmacılara çözümleme sunucularına erişim veriyor. Sekiz kişilik bir ekip bunu işletiyor. Bir araştırmacının korumasız bir veri kümesini kişisel bir bulut klasörüne kopyaladığı bir olaydan sonra, üniversitenin güvenlik görevlisi her değişikliğin ve her erişim talebinin üç haftalık bir güvenlik gözden geçirmesinden geçmesini talep ediyor. Araştırmacılar bunun hizmeti kullanılamaz hale getireceğine itiraz ediyor.

Hizmet yöneticisi farklı bir yaklaşım öneriyor ve güvenlik görevlisi ile iki araştırmacıyla buluşuyor. Tutulan bilgiyi listeliyorlar ve veri kümelerini herkese açık, dahili ve hassas olarak grupluyorlar. Hassas veriler için daha sıkı denetimler üzerinde uzlaşıyorlar: adlandırılmış role ve projeye göre erişim, hizmetin dışında kopya yok ve veri dışa aktarımının günlüğe kaydedilmesi. Diğer veriler için daha hafif kurallar geçerli. Ekip, teslimat hattına yanlış yapılandırılmış depolama ve koddaki sırlar için otomatik denetimler ekliyor ve güvenlik görevlisi her değişikliği gözden geçirmek yerine sonuçları haftalık gözden geçiriyor. Hassas veri kümeleri için erişim talepleri, projenin veri sorumlusunun onayını ve bir son kullanma tarihini içeren bir talep modelini izliyor. Araştırmacılar için önceki olaya dayalı kısa bir eğitim oturumu yapılıyor.

Altı ay sonra hizmetin dışında başka kopya bulunmadı ve erişim gözden geçirmeleri her çeyrekte bir öğleden sonra sürüyor. Bazı zorluklar sürüyor. Bir grup araştırmacı, verileri günlüğün yakalamadığı bir biçimde dışa aktaran bir araç kullanıyor ve otomatik denetimler ekibin yok saymaya başladığı yanlış alarmlar üretiyor. Güvenlik görevlisiyle aracı günlükleme kapsamına eklemeyi, denetimleri ayarlamayı ve uyarıları aylık gözden geçirmeyi kabul ediyorlar. Ayrıca olay planının kaynağı alıntılayabilmesi için hukuk ekibinden hassas veri kümeleri için geçerli bildirim yükümlülüklerinin yazılı bir beyanını istiyorlar.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri güvenliği kodda ve yapılandırmada gerçek kılar. Tehditleri erken tartışın, sırları koddan uzak tutun, otomatik bulgulara yanıt verin ve hassas verileri sınamalarda paylaşmaktan kaçının. Maruziyeti değiştiren değişiklikleri güvenliğe ve operasyona bildirin.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri denetimleri yürütür: erişim, izleme, yamalama ve yedekler. Güvenlik etkinliklerini olay olarak ele alın, delili koruyun ve tatbikatlara katılın. Olay örüntülerini teslimata ve risk kaydına geri besleyin.

### Liderlik ve yönetişim

Liderler risk kararlarına ve etrafındaki kültüre sahiptir. Sade dilli risk özetleri isteyin, eğitim ve tatbikatlar için zamanı destekleyin ve bir riski kabul etme kararının her biri için birinin hesap verebilir olduğundan emin olun. Belgelendirmeyi nedensiz bir etiket olarak talep etmeyin.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar hizmete bilgilerini emanet eder. Sunulduğunda güçlü kimlik doğrulama kullanın, şüpheli iletileri bildirin ve sağlayıcılara verilerinizi nasıl koruduklarını ve bir ihlali size nasıl bildireceklerini sorun. Bir şey ters gittiğinde dürüstlük ve hız bekleyin.

## Yaygın başarısızlık biçimleri

- **Son kapı olarak güvenlik.** Gözden geçirmeler sonda gelir ve sürümleri geciktirir. Bunun yerine tehditleri erken tartışın ve denetimleri teslimat hattında otomatikleştirin.
- **Hedef olarak uyum.** Bir belge zayıf uygulamayı gizler. Bunun yerine standartları yapı için kullanın ve gerçek korumayı ölçün.
- **İzlenmeyen veri.** Kopyalar sınama sistemlerine ve kişisel depolamaya yayılır. Bunun yerine hassas verinin nerede yaşadığını bilin ve kopyaları sınırlayın.
- **Fazla erişim.** Haklar birikir ve hiç kaldırılmaz. Bunun yerine erişimi düzenli olarak gözden geçirin ve süresini bitirin.
- **Kodda sırlar.** Kimlik bilgileri depolarda saklanır. Bunun yerine bir kasa kullanın ve sırları döndürün.
- **Sınanmış olay planı yok.** İlk kullanım gerçek bir ihlaldir. Bunun yerine planı uygulayın ve bildirim yükümlülüklerini yazın.
- **Hatalar için suçlama.** İnsanlar hataları gizler. Bunun yerine bildirmeyi kolaylaştırın ve öğrenmeyle yanıt verin.
- **Tedarikçileri göz ardı etmek.** Üçüncü taraflar net korumalar olmadan veri tutar. Bunun yerine sorun, sözleşmeye bağlayın ve gözden geçirin.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Bilgi ve risk | Hassas veri listelenmemiştir; riskler örtüktür | Bazı hizmetler veri türlerini ve riskleri kaydeder | Veri ve riskler hizmet başına sahipler ve kararlarla kaydedilir | Riskler olaylara ve ölçülere karşı gözden geçirilir | Risk görünümleri müşteriler ve tedarikçilerle paylaşılır ve hizalanır |
| Teslimatta denetimler | Güvenlik gözden geçirmesi, varsa sonda yapılır | Bazı ekipler güvenlik taraması yapar | Güvenlik denetimleri ortak bir teslimat hattında otomatiktir, bulguların sahipleri vardır | Bulgular, düzeltmeler ve kaçaklar ölçülür ve gözden geçirilir | Denetimler ortak kanıttan ekipler arasında geliştirilir |
| Erişim ve sırlar | Erişim ad hoc verilir; sırlar kodda | Bazı gözden geçirmeler ve kasalar vardır | Süre sonlu rol tabanlı erişim ve yönetilen sırlar standarttır | Erişim gözden geçirmeleri ve döndürme ölçülür | Erişim ve sır uygulamaları ortaklarla eşgüdümlüdür |
| Olay müdahalesi ve kültür | Güvenlik olayları doğaçlamadır | Bazı planlar vardır | Güvenlik olayları, tanımlı ek adımlarla olay sürecini izler ve uygulanır | Algılama ve yanıt süreleri ölçülür ve öğrenme paylaşılır | Yanıt tedarikçiler, müşteriler ve yetkililerle eşgüdümlüdür |

## Kontrol listesi

- [ ] Başlıca bilgi türlerini, sahiplerini, konumlarını ve hassasiyetlerini listeledik.
- [ ] Önemli hizmetler için gizlilik, bütünlük ve erişilebilirlik riskleri değerlendirilir ve kararlar kaydedilir.
- [ ] Otomatik güvenlik denetimleri her değişiklikte çalışır ve bulguların sahipleri vardır.
- [ ] Erişim role ve ihtiyaca göredir, düzenli olarak gözden geçirilir ve artık gerekmediğinde kaldırılır.
- [ ] Sırlar yönetilen bir kasada saklanır ve hızla döndürülebilir.
- [ ] Bir güvenlik olayı planı vardır, uygulanmıştır ve kaynak metniyle birlikte bildirim yükümlülüklerini içerir.
- [ ] Bilgimizi tutan tedarikçilere korumaları sorulmuştur.
- [ ] Personel kısa, düzenli eğitim alır ve hataları suçlanmadan bildirebilir.
- [ ] ISO/IEC 27001 kullanıyorsak gerekçeli bir Uygulanabilirlik Bildirimimiz ve hafif bir ISMS'miz var.
- [ ] Ramak kalalar örüntüler açısından gözden geçirilir.

## Yapay zeka istemleri

**Amaç: bilginizin envanterini çıkarmak ve hassasiyete göre sıralamak.**

```text
Help me make a simple inventory of the information our service holds.

What the service does: [describe].
Data we know about (types, where stored, who can access): [paste a list; remove any real personal data].
Rules or contracts that apply, with source text: [paste, or write "none known"].

Produce a table with: information type, where it lives, who owns it, a suggested sensitivity level (public, internal, sensitive) with a one-sentence reason from my text, and one question to ask about protection. Mark guesses. Do not state that any law applies unless I pasted its text. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: yeni bir özellik için kısa bir tehdit tartışması yürütmek.**

```text
Help me run a 30-minute threat discussion for this new feature: [describe what it does, what data it handles, who uses it, and what it connects to].

Provide questions to ask under these headings: who might misuse it and how; what data could be exposed, changed, or made unavailable; what could go wrong through dependencies or suppliers; what we would see if it went wrong; and what safeguards we already have. Then give a template for recording risks with an owner and a decision (accept, reduce, transfer, or avoid). Do not invent attacks or vulnerabilities in my system. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: otomatik güvenlik bulgularını gürültü ve öncelik açısından gözden geçirmek.**

```text
Here are findings from our automated security checks in the last [period]: [paste, with counts and short descriptions; remove sensitive details].
What we did about each (fixed, suppressed, ignored): [paste, or write "unknown"].

Group the findings by type. For each group, suggest a question to ask about whether it is noise, a real risk, or a tool configuration issue, using only the text. Identify which groups are most often ignored. Do not state that a finding is exploitable or harmless. Suggest how to assign owners. List what you are unsure of.
```

**Amaç: bir güvenlik olayı tatbikatı hazırlamak.**

```text
Design a 60-minute tabletop exercise on a suspected data breach in [service].

Scenario basis: [describe, using facts you choose, for example "a laptop with access to production data is reported lost"].
Roles taking part: [list].
Notification duties that apply, with source text from legal or compliance: [paste, or write "not yet confirmed"].

Give a timed plan, prompts for each role (contain, preserve evidence, communicate, decide who is told), a list of decisions that need authority, and a closing step that records gaps with owners. Do not use real data or systems. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Yapay zeka becerileri

- [security-testing](../../../../skills/security-testing/SKILL.md): teslimat döngüsünün parçası olarak güvenlik sınamalarını planlamak için kullanın.
- [risk-register](../../../../skills/risk-register/SKILL.md): güvenlik risklerini, kararları ve sahipleri kaydetmek için kullanın.
- [key-risk-indicators](../../../../skills/key-risk-indicators/SKILL.md): güvenlik riskleri için erken uyarı ölçüleri seçmek için kullanın.
- [data-governance](../../../../skills/data-governance/SKILL.md): verinin sahibinin kim olduğunu ve nasıl kullanılıp paylaşılabileceğini tanımlamak için kullanın.
- [legal-data-privacy-compliance](../../../../skills/legal-data-privacy-compliance/SKILL.md): hukuk ya da uyum personeline mahremiyet yükümlülükleri hakkında sorular hazırlamak için kullanın.

## Temel kaynaklar

- **Information security** (Wikipedia): CIA üçlüsü, risk yönetimi, denetimler ve olay müdahalesi, ilgili standartların ve yasaların uzun bir listesiyle birlikte.
- **ISO/IEC 27001** (Wikipedia ve ISO'nun standardın kendisi): Ek A denetimleri ve belgelendirme süreciyle birlikte bir bilgi güvenliği yönetim sisteminin şartları.
- **Computer security incident management** (Wikipedia): güvenlik etkinliklerine yanıt verme üzerine arka plan.
- **Defense in depth** (Wikipedia): katmanlı denetimler üzerine arka plan.

## Kaynakça

1. Information security — Wikipedia — https://en.wikipedia.org/wiki/Information_security
2. ISO/IEC 27001 — Wikipedia — https://en.wikipedia.org/wiki/ISO/IEC_27001
3. ISO/IEC 27002 — Wikipedia — https://en.wikipedia.org/wiki/ISO/IEC_27002
4. Computer security incident management — Wikipedia — https://en.wikipedia.org/wiki/Computer_security_incident_management
5. Defense in depth (computing) — Wikipedia — https://en.wikipedia.org/wiki/Defense_in_depth_(computing)
6. Risk management — Wikipedia — https://en.wikipedia.org/wiki/Risk_management
7. Principle of least privilege — Wikipedia — https://en.wikipedia.org/wiki/Principle_of_least_privilege
8. Continuous delivery — DORA, dora.dev — https://dora.dev/capabilities/continuous-delivery/
9. Incident management — Wikipedia — https://en.wikipedia.org/wiki/Incident_management
