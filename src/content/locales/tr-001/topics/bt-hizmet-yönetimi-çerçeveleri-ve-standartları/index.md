# BT Hizmet Yönetimi Çerçeveleri ve Standartları

**BT hizmet yönetiminin birbiriyle örtüşen birçok çerçevesi ve standardı vardır; yararlı beceri, her birinin ne için olduğunu bilmektir: öğrenilecek bir rehberlik mi, karşısında belgelendirilebileceğiniz bir standart mı, yoksa neyi denetleyeceğinizi söyleyen bir yönetişim modeli mi.**

## Bu neden önemli

Beş kişiye "ITSM en iyi uygulamasını izliyoruz" ifadesinin ne anlama geldiğini sorun; beş yanıt alabilirsiniz: ITIL, ISO/IEC 20000, COBIT, FitSM ya da "tedarikçinin aracı ne yapıyorsa." Terimler gevşek biçimde kullanılır ve farklar önemlidir. ISO/IEC 20000 belgelendirmesi isteyen bir müşteri, ITIL eğitimiyle memnun edilemez. COBIT kontrollerini soran bir denetçiye bir hizmet masası süreç haritası yardımcı olmaz.

Çevik ekipler için soru pratiktir: bunlardan hangileriyle uğraşmak zorundayız ve hangilerini fikir kaynağı olarak görebiliriz? Birçok ekip, en bilineni ITIL'in kuruluşlar için bir standart değil, bireylerin sertifika alabildiği bir rehberlik olduğunu öğrenince şaşırır. Diğerleri ise ana ITSM standardının yakın zamanda çevik ve DevOps çalışma biçimlerine dair rehberlik eklediğini öğrenince şaşırır.

Bu konu ana çerçeveleri ve standartları, [BT hizmet yönetimi](https://en.wikipedia.org/wiki/IT_service_management), [ISO/IEC 20000](https://en.wikipedia.org/wiki/ISO/IEC_20000), [COBIT](https://en.wikipedia.org/wiki/COBIT) ve [FitSM](https://en.wikipedia.org/wiki/FitSM) hakkındaki Wikipedia maddelerini kullanarak karşılaştırır. Bu maddelerin kalitesi değişkendir ve birkaçı bakım işaretleri taşır. Zayıf oldukları yerde bu konu bunu söyler. Bir sözleşme veya denetim için herhangi bir ayrıntıya güvenmeden önce sahiplerinin kendi yayınlarını kontrol edin.

## Temel kavramlar

### Üç tür şey

Bu konudaki adlar üç gruba ayrılır. Onları ayrı tutmak birçok kafa karıştıran konuşmayı önler.

| Tür | Size ne verir | ITSM hakkındaki Wikipedia maddesinde adı geçen örnekler |
|---|---|---|
| **Rehberlik (çerçeve veya kütüphane)** | Uyarlanacak fikirler ve anlatılmış uygulamalar | ITIL, Microsoft Operations Framework, Application Services Library, Business Information Services Library |
| **Belgelendirilebilir bir standart** | Bir kuruluşun denetlenebileceği ve belgelendirilebileceği gereksinimler | ISO/IEC 20000 |
| **Bir yönetişim veya yetkinlik modeli** | BT'yi yönlendirmenin, denetlemenin veya değerlendirmenin bir yolu | COBIT, CMMI, TOGAF |

FitSM, aşağıda anlatıldığı gibi ilk ikisinin arasında yer alır.

### ITIL

ITIL, ITSM ve BT varlık yönetimi üzerine rehberliktir. Sertifikasyon bireyler içindir ve bir kuruluşun ITIL uyumuna dair bağımsız bir değerlendirme yoktur (bkz. Konu 2.2 — ITIL). En yaygın kullanılan sözcük dağarcığı kaynağıdır.

### ISO/IEC 20000

ISO/IEC 20000, BT hizmet yönetimi için uluslararası bir standarttır. Wikipedia'ya göre Bölüm 1, hizmetlerin planlanmasını, sunulmasını ve iyileştirilmesini kapsayan bir hizmet yönetim sistemi için gereksinimleri belirler. BSI Group tarafından oluşturulan BS 15000'den geliştirilmiş ve ilk kez Aralık 2005'te yayımlanmıştır. Güncellemeler izlemiştir: Haziran 2011'de Bölüm 1 ve 15 Temmuz 2018'de yayımlanan, ardından belgelendirilmiş kuruluşlara üç yıllık geçiş süresi tanınan ikinci revizyon ISO/IEC 20000-1:2018. 2018 sürümü, ISO üst düzey yapısını izleyen on maddeye sahiptir.

Standardın birçok bölümü vardır. Madde, diğerlerinin yanı sıra şunları listeler: bir hizmet yönetim sisteminin uygulanması hakkında rehberlik (Bölüm 2); kapsam ve uygulanabilirlik hakkında rehberlik (Bölüm 3); uygulama rehberliği (Bölüm 5); belgelendirme kuruluşları için gereksinimler (Bölüm 6); kavramlar ve sözcük dağarcığı (Bölüm 10); ve ITIL 4 ile ilişkiye dair teknik bir şartname (Bölüm 11). Ayrıca 2023'ten 2025'e kadar yakın zamanda yayımlanan, hizmet entegrasyonu ve yönetimi (SIAM), çevik ve DevOps ile sürdürülebilirlik hakkında rehberlik içeren bölümleri listeler. Wikipedia hangi bölüm numarasının hangi konuyu kapsadığını söylemez; bu nedenle birini anmadan önce ISO kataloğuna bakın.

Kuruluşlar belgelendirilebilir ve bireyler APMG-International, EXIN ve PECB gibi kuruluşlardan yeterlilik kazanabilir. Madde, 2024 ISO anketinin 27.332 sertifika saydığını ve bunların 24.056'sının Çin'de olduğunu bildirir. Bu, belgelendirmenin ülkeler arasında ne kadar eşitsiz dağıldığını gösterir; bu nedenle başka bir yerdeki bir müşterinin bunu isteyeceğini varsaymayın.

Wikipedia, standardın başlangıçta ITIL en iyi uygulamasını yansıtmak üzere geliştirildiğini söyler, ancak bu iddiayı "citation needed" olarak işaretler. İlişkiyi yakın ama özdeş olmayan bir ilişki olarak görün. Madde ayrıca standardın Microsoft Operations Framework ve COBIT'in bazı bölümleri gibi diğer çerçeveleri desteklediğini söyler.

### COBIT

COBIT, Wikipedia'ya göre ISACA tarafından BT yönetimi ve yönetişimi için oluşturulmuş bir çerçevedir. İş hedeflerini BT hedeflerine bağlar ve iş ile BT ekipleri için sorumlulukları tanımlar. Madde beş süreç alanını anlatır: Değerlendir, Yönlendir ve İzle; Hizala, Planla ve Örgütle; Oluştur, Edin ve Uygula; Sun, Hizmet Ver ve Destekle; ve İzle, Değerlendir ve Ölç. Şu tarihleri verir: ilk olarak 1996'da yayımlanmış, sürüm 5 2012'de çıkmıştır ve ISACA'nın COBIT 2019 ve COBIT 5 için sertifikasyon sunduğunu söyler. Madde COBIT'i ITIL, ISO 27000, CMMI, TOGAF ve Proje Yönetimi Enstitüsü'nün PMBOK Kılavuzu'na bağlar.

Maddenin kendisi birincil kaynaklar ve eksik atıflar hakkında bakım işaretleri taşır ve çerçevenin şirketlerin yasaya uymasına ve daha çevik olmasına yardımcı olduğu yönündeki bir iddia tek bir kaynağa dayanır. Otorite için COBIT'in kendi yayınlarını kullanın.

### FitSM

FitSM, bir hafif standartlar ailesidir. Wikipedia, bunun federe e-altyapılarda hizmet yönetimini iyileştirmek için AB tarafından finanse edilen bir proje olan FedSM'den doğduğunu ve gözden geçirilmiş çıktıların Mayıs 2013'ten itibaren FitSM adıyla yayımlandığını söyler. FitSM-1, genel gereksinimleri ve 14 süreci kapsayan yaklaşık 85 denetlenebilir gereksinim içerir ve kapsam ve üslup bakımından benzer olmasına rağmen ISO/IEC 20000 Bölüm 1'den çok daha kısadır. Tüm bölümler Creative Commons lisansları altında yayımlanır. Kuruluşlar FitSM uyumlu olarak belgelendirilemez, ancak uyum denetlenebilir ve 2013'te bir personel sertifikasyon şeması başlamıştır.

FitSM, kısa bir gereksinim kümesi isteyen küçük ekipler için yararlıdır. Madde mevcut sürümü veya onu sürdüren grubun durumunu belirtmez; bu nedenle güvenmeden önce bunları doğrulayın.

### Diğer adlar

ITSM maddesi ayrıca aşağıdakileri listeler. Bu kılavuz bunları daha fazla ele almaz.

- **CMMI:** hizmetleri ve süreçleri oluşturmak, yönetmek ve iyileştirmek için bir model.
- **TOGAF:** iş hedeflerini mimari hedeflere bağlayan bir çerçeve.
- **Microsoft Operations Framework:** Microsoft teknolojilerine dayalı hizmet yönetimi rehberliği.
- **Application Services Library ve Business Information Services Library:** uygulama yönetimi ve bilgi yönetimi için çerçeveler.
- **USM:** Hollanda hükümeti tarafından benimsenen, ilke temelli bir sistem.

Madde, ITSM çerçevelerinin ISO 9000, ISO/IEC 27000 ve CMMI'dan yararlandığını ekler. Güvenlik yönetiminin kendi standartlar ailesi vardır (bkz. Konu 3.13 — Bilgi Güvenliği Yönetimi).

### Standartlarda çevik ve DevOps

ISO/IEC 20000 maddesi, standardın çevik ve DevOps hakkında rehberlik içeren yakın tarihli bir bölümünü listeler. Bu dikkate değerdir, çünkü standart kuruluşunun çevik çalışma biçimlerini bir hizmet yönetim sisteminin karşılaması gereken bir şey olarak ele aldığını gösterir. Madde içeriğine dair ayrıntı vermez; bu nedenle ona ihtiyaç duyarsanız standardın kendisini okuyun. Bu arada ITIL 4 kendisini çevik, DevOps ve yalın ile uyumlu olarak tanımlar (bkz. Konu 2.2 — ITIL) ve ITSM hakkındaki Wikipedia maddesi çevikten hiç söz etmez. Kaynaklar, ne kadar yetiştikleri konusunda farklılık gösterir.

### Seçmek

Tek bir doğru çerçeve yoktur. Makul bir seçim yolu, neye ihtiyacınız olduğunu sormaktır:

| İhtiyacınız olan… | Düşünebileceğiniz… |
|---|---|
| Uygulamalar için ortak bir sözcük dağarcığı ve fikirler | ITIL |
| Müşteriler veya ihaleler için hizmet yönetim sisteminizin belgelendirilmesi | ISO/IEC 20000 |
| Küçük bir ekip için kısa, denetlenebilir bir gereksinim kümesi | FitSM |
| Kurumda BT'nin iş hedeflerine bağlı yönetişimi ve denetimi | COBIT |
| Süreç yetkinliğinin değerlendirilmesi | CMMI |

Bu tablo kılavuzun özetidir; herhangi bir çerçeve sahibinin önerisi değildir.

## İyi uygulamalar

1. **Yanıtlamanız gereken soruyla başlayın.** Neye ihtiyacınız olduğunu yazın: sözcük dağarcığı, belgelendirme, denetim veya değerlendirme. En iyi pazarlamaya sahip olanı değil, bunu yanıtlayan çerçeveyi seçin.
2. **Rehberlik ile standart arasındaki farkı öğrenin.** Ekibe ITIL sertifikasyonunun bireyler için, ISO/IEC 20000 sertifikasyonunun kuruluşlar için olduğunu ve COBIT'in bir yönetişim modeli olduğunu öğretin. Birçok sözleşme ve denetim karışıklığı buradan başlar.
3. **Müşterilerin ve düzenleyicilerin gerçekte neyi gerektirdiğini öğrenin.** Tam maddeyi veya gereksinimi isteyin. Çoğu zaman istek "tanınmış bir çerçeve" içindir ve uygulamanızın kısa, dürüst bir tanımı yeterlidir.
4. **Uyum için özetleri değil, standart metnini kullanın.** Uyum iddia ettiğinizde ISO standardından veya çerçeve sahibinin yayınından çalışın. Bu özet dâhil, özetler yalnızca yönelim içindir.
5. **Uygulamanızı dört kez değil, bir kez haritalayın.** Birden fazla çerçeveyi karşılamak zorundaysanız, ayrı belgeler yazmak yerine uygulamanızın tek bir tanımını oluşturun ve her birine eşleyin.
6. **Sistemi olabildiğince küçük tutun.** ISO/IEC 20000 bir hizmet yönetim sistemi ve kayıtlar ister. Her gereksinimi işe yarayan en hafif yaklaşımla karşılayın ve kanıtı araçlarınızdan otomatikleştirin.
7. **Kapsama dikkat edin.** Bir sertifika belirtilmiş bir kapsamı kapsar. Gerçek hizmetleri ve ekipleri yansıtan bir kapsam seçin ve sertifikayı zorlaştıran kısımları dışarıda bırakmayın.
8. **Kullandığınız standartlardaki çevik ve DevOps rehberliğini kontrol edin.** Bir standardın çevik ve DevOps hakkında rehberliği varsa, çevik bir ekibin bir gereksinimi nasıl karşılayabileceği konusunda bir denetçiyle tartışmadan önce onu okuyun.
9. **Küçük ekipler için daha hafif seçenekleri düşünün.** FitSM veya ITIL'in bir alt kümesi, küçük bir ekibe tam belgelendirilmiş bir sistemden daha iyi uyabilir. Dış belgelendirme gibi nelerden vazgeçtiğinizi not edin.
10. **Güvenlik ve hizmet yönetimini uyumlu tutun.** Bilgi güvenliği için ISO/IEC 27001 kullanıyorsanız, çift iş yapmamak için kayıtları ve gözden geçirmeleri hizmet yönetim sisteminizle paylaşın (bkz. Konu 3.13 — Bilgi Güvenliği Yönetimi).
11. **Uyarlamanızı belgeleyin.** Bir çerçevenin hangi kısımlarını kullandığınızı, hangilerini kullanmadığınızı ve nedenini kaydedin. Bu sizi denetimlerde korur ve yeni personele yardımcı olur.
12. **Yıllık gözden geçirin.** Standartlar ve çerçeveler değişir. Güncellemeleri izlemesi ve ekibiniz için önemli olanı bildirmesi için birini görevlendirin (bkz. Konu 6.4 — Öğrenme Yolları ve Sertifikasyon).

## Ekibinizle tartışılacak sorular

**Bu çerçevelerden veya standartlardan hangilerini kullanmak zorundayız ve hangilerini alışkanlıkla kullanıyoruz?**

Müşterilerin, sözleşmelerin, düzenleyicilerin ve yöneticilerin gerçekte ne istediğini, bunu söyleyen belgeyle birlikte listeleyin. Ardından ekibin bir gereksinim olmadan kullandıklarını listeleyin. İki liste çoğu zaman beklenenden daha fazla farklılaşır. Kolaylaştırıcı, her birini ilk kimin getirdiğini ve nedenini sorabilir. İşi yönlendiren herhangi bir gereksinimin tam ifadesini bularak sürdürün.

**Bir müşteri "ITIL sertifikalı mısınız" diye sorsa ne yanıtlardık?**

Dürüst bir yanıtı deneyin: bireyler sertifikalandırılabilir, kuruluşlar sertifikalandırılamaz ve işte yaptığımız şey. Yanıtları karşılaştırın. Bazıları abartacaktır. Müşterinin muhtemelen neye ihtiyaç duyduğunu ve hangi kanıtın bunu karşılayabileceğini, örneğin ISO/IEC 20000 belgelendirmesini veya uygulamanın bir tanımını tartışın. Herkesin kullanabileceği bir cümle üzerinde anlaşın.

**ISO/IEC 20000 belgesi almak bize neye mal olurdu ve ne kazanırdık?**

Hangi müşterilerin veya pazarların buna değer vereceğini ve ekibin neyi değiştirmesi gerekeceğini sorun. Maliyetler hakkında tahmin yürütmeyin; gerçek teklifler toplayın veya bunu yapmış bir meslektaşa sorun. Anlatabileceğiniz yararları listeleyin: tanınmış bir etiket, disiplinli bir sistem, ihalelere erişim. Daha fazla araştırıp araştırmayacağınıza karar verin.

**Denetim kayıtlarımız nereden geliyor ve araçlarımız bunları otomatik olarak üretebilir mi?**

Denetçilerin istediği kayıtları ve her birinin nereden geldiğini listeleyin. Birçoğu, bunu akılda tutarak yapılandırıldıklarında sürüm denetimi, bilet araçları ve izlemeden gelebilir. Hangi kayıtların elle üretildiğini ve nedenini sorun. Otomatikleştirilecek bir tane seçin.

**Çevik uygulamalarımız standartların beklediği şeye nasıl uyuyor ve boşluk nerede?**

Denetçinizin önem verdiği bir gereksinimi, örneğin değişiklik yetkilendirmesini alın ve çevik bir ekibin bunu nasıl karşıladığını anlatın. Standardın çevik ve DevOps hakkında rehberliği varsa ilgili metni birlikte okuyun. Niyette değil, kanıtta boşlukları not edin.

**Bu çerçevelerdeki değişiklikleri bizim için kim izliyor?**

Çerçeve sahiplerinin ve standart kuruluşlarının duyurularını kimin okuduğunu sorun. Sık verilen yanıt "kimse"dir. Kimin okuyacağına, nasıl rapor vereceğine ve ne zaman vereceğine karar verin. Kolaylaştırıcı, neyin değiştiğini ve önemli olup olmadığını listeleyen üç ayda bir kısa bir not önerebilir.

## Uygulamada: çevik bir ITIL örneği

120 kişilik bir yazılım şirketi, hastanelere ve üniversitelere barındırılan bir randevu ürünü satar. Büyük bir üniversite müşterisinin ihalesi "belgelendirilmiş bir BT hizmet yönetim sistemi" şart koşar. Kurucular, ITIL eğitimli destek liderinin yeteceğini varsaymıştı. Destek lideri, ITIL sertifikasyonunun bireyler için geçerli olduğunu ve ihalenin büyük olasılıkla ISO/IEC 20000'i kastettiğini açıklar.

Operasyon başkanı araştırır. ISO/IEC 20000-1'i anan ihale metnini okur ve müşteriye hangi kapsamı beklediklerini sorar. Standardın içindekiler tablosunu okur ve on maddesini şirketin çoğunlukla bilet aracından, değişiklik geçmişinden ve olay gözden geçirmelerinden gelen mevcut kayıtlarıyla karşılaştırır. Kanıtın büyük bölümünün zaten var olduğunu, ancak belgelenmiş hizmet yönetimi politikalarının, resmî tedarikçi gözden geçirmelerinin ve yönetim gözden geçirmesinin olmadığını görür. Ayrıca standardın artık çevik ve DevOps rehberliğine dair bir bölümü olduğunu bulur; bu, şirketin haftalık sürümlerini olası bir denetçiye açıklamasına yardımcı olur.

Şirket, yalnızca barındırılan ürün için, mütevazı bir belge kümesi ve üç ayda bir yönetim gözden geçirmesiyle belgelendirmeyi sürdürmeye karar verir. Yaklaşık bir yıllık çalışma planlar. Her şey sorunsuz gitmez. İki mühendis ek kayıtlara direnir ve bir tedarikçi resmî hizmet gözden geçirme raporları sağlamayı reddeder. Operasyon başkanı bazı elle tutulan kayıtları şirketin araçlarından dışa aktarımlarla değiştirir ve tedarikçiyle daha hafif bir gözden geçirme düzenlemesi için pazarlık yapar. Şirket ihaleyi kazanır ve bir sonraki gözetim denetiminde sistemin haftalık sürümlere yardımcı olup olmadığını ya da engel olup olmadığını gözden geçirmeye karar verir.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri bu çerçevelerle müşterilerden ve denetçilerden gelen gereksinimler olarak karşılaşır. Hangi gereksinimin geçerli olduğunu öğrenin ve hangi kanıtın kabul edilebilir olduğunu sorun. Birçok gereksinim, zaten kullandığınız araçlardan karşılanabilir. Sürüm sürecinizi standardın diliyle açıklamayı önerin.

### Hizmet ve operasyon ekipleri

Yönetim sistemini genellikle operasyon ekipleri taşır. Kayıtları, her birinin belirtilmiş bir amacıyla yararlı tutun. Çerçeveler arasında birbirini tekrarlayan gereksinimlere dikkat edin ve bunları bir kez haritalayın. Kayıtların ayrı bir görev değil, işin yan ürünü olması için planı teslimat ekipleriyle paylaşın.

### Liderlik ve yönetişim

Liderler hangi çerçevelerin benimseneceğine ve belgelendirmeye ne kadar yatırım yapılacağına karar verir. İş gerekçesinin ne olduğunu ve müşterilerin gerçekte neyi gerektirdiğini sorun. Belgelendirmeyi bir etiket olarak satın almaya karşı dikkatli olun. Sistemin kuruluşun iyileşmesine yardımcı olduğundan ve birinin ona sahip olduğundan emin olun.

### Müşteriler ve kullanıcılar

Belgelendirme isteyen müşteriler çoğu zaman güvence ister. Sağlayıcılara sertifikalarının hangi standardı ve kapsamı kapsadığını ve neyin dışarıda kaldığını sorun. Bir sertifika, bir yönetim sisteminin kanıtıdır; herhangi bir bireysel sonucun garantisi değildir.

## Yaygın başarısızlık biçimleri

- **Bireysel ve kurumsal sertifikasyonu karıştırmak.** Ekipler bir şirket için "ITIL sertifikalı" der. Bunun yerine neyin kim tarafından belgelendirildiğini tam olarak belirtin.
- **Sertifikasyonu bir etiket olarak kovalamak.** Sistem iyileştirme için değil, denetim için vardır. Bunun yerine önce kayıtları ekip için yararlı hâle getirin.
- **Çerçeveler arasında belgeleri çoğaltmak.** Her standarda kendi klasörü verilir. Bunun yerine uygulamanızı bir kez tanımlayın ve eşleyin.
- **Zor kısımlardan kaçınmak için kapsamı daraltmak.** Sertifika, müşterilerin önemsediği hizmetleri dışarıda bırakır. Bunun yerine gerçek hizmetleri yansıtan bir kapsam seçin.
- **Özetlere güvenmek.** Uyum iddiaları blog yazılarına dayanır. Bunun yerine standardın veya çerçeve sahibinin metninden çalışın.
- **Çevik rehberliği yok saymak.** Ekipler, standardın çevik ve DevOps'u ele alan bölümünü okumadan denetçilerle tartışır. Bunun yerine onu okuyun ve örnekler hazırlayın.
- **Aşırı belgelendirme.** Sistem kimsenin okuduğundan fazla kayıt üretir. Bunun yerine her kaydı bir amaca bağlayın ve kanıtı otomatikleştirin.
- **Değişiklikleri unutmak.** Standart ilerler ve ekip fark etmez. Bunun yerine güncellemeleri izlemesi için birini adlandırın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Çerçeveleri anlama | Adlar gevşek biçimde kullanılır | Bazı personel her çerçevenin ne için olduğunu söyleyebilir | Ekipler kullanılan çerçevelerin kısa, doğru bir tanımını paylaşır | Çerçevelerin kullanımı gereksinimlere ve sonuçlara göre gözden geçirilir | Ekipler, müşteriler ve tedarikçiler doğru bir anlayışı paylaşır |
| Gereksinimler ve kapsam | Gereksinimler varsayılır | Bazı gereksinimler belgelere kadar izlenir | Gereksinimler ve kapsam belgelenmiştir | Uyum ve kapsam gözden geçirilir ve boşluklar izlenir | Gereksinimler ortaklar ve müşterilerle uyumlandırılır |
| Kanıt | Kanıt her talep için elle derlenir | Bazı kayıtlar araçlardan üretilir | Kanıt çoğunlukla araçlardan gelir ve tutarlı biçimde tanımlanır | Kanıt kalitesi ölçülür ve iyileştirilir | Kanıt denetçiler ve ortaklarla otomatik olarak paylaşılır |
| Güncellik | Çerçevelerdeki değişiklikler fark edilmez | Bazı kişiler duyuruları izler | Adlandırılmış bir kişi değişiklikleri belirli aralıklarla bildirir | Değişiklikler değerlendirilir ve onlara göre hareket edilir | Değişiklikler öngörülür ve ortaklarla ele alınır |

## Kontrol listesi

- [ ] Müşterilerin, sözleşmelerin veya düzenleyicilerin gerçekte hangi çerçeveleri ve standartları gerektirdiğini söyleyebiliyoruz.
- [ ] Hangilerinin rehberlik, hangilerinin belgelendirilebilir standart ve hangilerinin yönetişim modeli olduğunu biliyoruz.
- [ ] Belgelendirme hakkındaki iddialarımız doğrudur ve kapsamı belirtir.
- [ ] Her uyum iddiası için standardın veya sahibinin metninden çalışıyoruz.
- [ ] Uygulamamız bir kez tanımlanmıştır ve karşılamamız gereken her çerçeveye eşlenmiştir.
- [ ] Denetimler için kanıt çoğunlukla araçlarımızdan gelir.
- [ ] Bizi ilgilendiren standartlardaki çevik ve DevOps rehberliğini okuduk.
- [ ] Güncellemeleri izlemek ve bildirmek için biri adlandırılmıştır.
- [ ] Uyarlama kararlarımız yazılıdır.
- [ ] Kapsamımızın gerçek hizmetlerle örtüşüp örtüşmediğini gözden geçirdik.

## Yapay zeka istemleri

**Amaç: bir müşteri gereksinimini onu destekleyen çerçeve metnine eşlemek.**

```text
A customer or auditor has made this requirement: [paste the exact wording and where it appeared, for example a tender clause].

Here is the text of the relevant standard or framework, which I have copied from the owner's publication: [paste only text you are entitled to use; keep it short].

Using only the pasted text, say what the requirement appears to ask for, what is unclear, and what questions I should put to the customer. Do not describe the contents of any standard that I have not pasted. Do not say whether we comply. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: uygulamanızı bir kez tanımlayarak birkaç çerçeveye eşlenebilir hâle getirmek.**

```text
Help me write a single plain-language description of how we handle [practice, e.g. "changes to production"].

How it works today, in steps, with the tools and records involved: [paste].
Frameworks we need to map it to: [list names; I will paste the relevant requirement text for each].

Produce a description in short numbered steps, then a table with one row per step and one column per framework showing which pasted requirement the step seems to address (only from my pasted text). Mark gaps as questions, not conclusions. Do not claim conformance. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: "ITIL sertifikalı mısınız?" sorusuna dürüstçe yanıt vermeye hazırlanmak.**

```text
Write a short, honest reply to a customer who asks whether our company is "ITIL certified."

Facts I have verified from official sources: [paste, for example that certification in ITIL applies to individuals; and list the certifications our staff hold].
What we actually do: [describe our practice in a few sentences].
Other certifications we hold or are considering: [list].

The reply should be polite, accurate, under 150 words, and avoid overclaiming. Offer evidence we could share. Use only the facts I gave. Ask clarifying questions first if anything is missing, and list what you are unsure of.
```

**Amaç: bir hizmet yönetimi denetiminin isteyebileceği kanıtı planlamak.**

```text
We expect an audit of our service management against [standard name and edition].

The records we produce today, and the tool each comes from: [list].
The requirement areas I know of, with the wording I have from the standard: [paste, or write "not yet read"].

Create a table of likely evidence by requirement area (from my pasted text only), the record we already have, the gap, and whether the record could come from a tool automatically. Do not invent requirements. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Yapay zeka becerileri

- [enterprise-architecture](../../../../skills/enterprise-architecture/SKILL.md): hizmet yönetimi çerçevelerini kurumsal mimari ve yönetişimin daha geniş resmine yerleştirmek için kullanın.
- [legal-compliance-audit](../../../../skills/legal-compliance-audit/SKILL.md): bir standarda veya sözleşme gereksinimine karşı bir denetime nasıl hazırlanılacağını planlamak için kullanın.
- [compliance-testing](../../../../skills/compliance-testing/SKILL.md): uyumun kanıtını otomatik olarak üreten kontroller tasarlamak için kullanın.
- [vendor-management](../../../../skills/vendor-management/SKILL.md): bir belgelendirme kapsamı tedarikçilere bağlı olduğunda ve tedarikçi gözden geçirmelerini planlamanız gerektiğinde kullanın.
- [project-management-body-of-knowledge](../../../../skills/project-management-body-of-knowledge/SKILL.md): COBIT veya PMBOK Kılavuzu gibi çerçeveler proje ofisinizle buluştuğunda kullanın.

## Temel kaynaklar

- **ISO/IEC 20000-1** (International Organization for Standardization): standardın kendisi; iddialarda bulunmadan önce kapsamını ve madde başlıklarını ISO kataloğunda okuyun.
- **ISO/IEC 20000** (Wikipedia): standardın tarihi, bölümleri ve belgelendirme ortamı; atıflarla birlikte.
- **COBIT** (ISACA ve Wikipedia): ISACA'nın kendi yayınları yetkilidir; Wikipedia maddesi tarih ve yapı sunar ancak kaynakları zayıftır.
- **FitSM** (Wikipedia ve FitSM projesi): kısa, serbestçe lisanslanmış bir alternatif; güncel sürüm için projenin sayfalarına bakın.

## Kaynakça

1. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
2. ISO/IEC 20000 — Wikipedia — https://en.wikipedia.org/wiki/ISO/IEC_20000
3. COBIT — Wikipedia — https://en.wikipedia.org/wiki/COBIT
4. FitSM — Wikipedia — https://en.wikipedia.org/wiki/FitSM
5. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
6. CMMI — Wikipedia — https://en.wikipedia.org/wiki/CMMI
7. TOGAF — Wikipedia — https://en.wikipedia.org/wiki/TOGAF
8. ISACA — Wikipedia — https://en.wikipedia.org/wiki/ISACA
9. ISO/IEC 27001 — Wikipedia — https://en.wikipedia.org/wiki/ISO/IEC_27001
10. Microsoft Operations Framework — Wikipedia — https://en.wikipedia.org/wiki/Microsoft_Operations_Framework
