# Yapay Zeka Becerileri ve İstemleri

**İyi bir istem, bir yapay zeka asistanına ihtiyaç duyduğu materyali, görevi ve kontrolleri verir; iyi bir beceri ise bu bilgi birikimini bir ekibin yeniden kullanabileceği biçimde paketler; bu da bu rehberdeki yapay zeka istemlerini ve becerilerini, uyarlayıp doğrulayacağınız başlangıç noktaları yapar.**

## Bu neden önemli

Bu rehberdeki her konu istemler ve becerilerle biter. Var olmalarının nedeni, hizmet yönetimindeki görevlerin birçoğunun, bir yığın bileti okuyabilen, bir çalıştırma kılavuzu (runbook) taslağı hazırlayabilen veya notları bir plana dönüştürebilen bir asistana çok uygun olmasıdır. Ayrıca yapay zekaya yapılan belirsiz bir isteğin belirsiz, bazen yanlış sonuçlar üretmesi de bir nedendir. Yararlı bir yanıt ile makul görünen ama boş bir yanıt arasındaki fark çoğu zaman isteğin nasıl yazıldığında ve yanında hangi materyalin geldiğinde yatar.

Bu konu, rehberin istemlerinin ve becerilerinin nasıl kullanılacağını, neden böyle yazıldıklarını ve ekibiniz için kendi istemlerinizi nasıl yazacağınızı açıklar. Hilelerden çok alışkanlıklarla ilgilidir: gerçek materyal sağlamak, ne istediğinizi söylemek, asistandan bilmediği şeyleri işaretlemesini istemek ve geri geleni kontrol etmek. Yapay zekanın nerede yardımcı olduğunu ve nerede zarar verebileceğini anlatan önceki konudaki uyarılara dayanır (bkz. Konu 6.2 — BT Hizmet Yönetiminde Yapay Zeka).

Kaynaklar pratiktir. Rehberin kendi `skills/prompt-engineering` becerisi, istem yazmayı bir dil modeline verilen talimatları tasarlamanın ve yinelemenin kasıtlı pratiği olarak, istemi yazılan, gerçek vakalara karşı test edilen ve gözden geçirilen küçük bir yazılım parçası gibi ele alarak tanımlar. Claude Code belgeleri, becerilerin bir `SKILL.md` dosyası olan dizinler olarak nasıl yapılandırıldığını anlatır. [Büyük dil modelleri hakkındaki Wikipedia maddesi](https://en.wikipedia.org/wiki/Large_language_model) arka plan bilgisi verir. Bu rehber için okunan hiçbir kaynak hangi istem tekniklerinin en iyi işlediğine dair kanıt sunmaz; buradaki teknikleri sınanacak alışkanlıklar olarak ele alın.

## Temel kavramlar

### İstemler, beceriler ve ne için oldukları

Bir **istem** (prompt), bir yapay zeka asistanına tek bir görev için verdiğiniz talimat ve materyaldir. Bir **beceri** (skill), bu rehberin `skills/` klasöründe kullanılan biçimiyle, bir tür görev için yeniden kullanılabilir bir bilgi birikimi paketidir: ne zaman kullanılacağını ve işin nasıl yapılacağını söyleyen bir `SKILL.md` dosyası içeren bir dizin. Claude Code belgelerinde bir beceri, ön bilgisi (frontmatter) bir ad ve bir açıklama içeren, gövdesi talimatları veren, zorunlu bir `SKILL.md` dosyası olan bir dizindir; asistan beceriyi ne zaman uygulayacağına karar vermek için açıklamayı kullanır ve gövdenin tamamını yalnızca kullanıldığında yükler.

| | İstem | Beceri |
|---|---|---|
| **Kapsam** | Tek bir görev, şimdi | Bir tür görev, yeniden kullanılan |
| **Nerede yaşar** | Bir sohbette veya belgede | `skills/` gibi bir klasörde veya bir projenin beceri dizininde |
| **Kim değiştirir** | Siz, her seferinde | Ekip, gözden geçirmeyle |
| **En uygun olduğu iş** | Kendi materyalinizin belirli analizi | Retrospektif yürütmek gibi yinelenebilir yöntemler |

### Rehberin istemleri nasıl kurulur

Bu rehberdeki istemler, stil kılavuzunda belirtilen basit bir örüntüyü izler:

1. **Kalın, tek satırlık bir amaç**, istemin ne için olduğunu söyler.
2. **Çitlenmiş bir blok**, kopyalayıp yapıştırabileceğiniz metni içerir.
3. **Köşeli parantez içindeki yer tutucular**, neyi sağlamanız gerektiğini, oraya ne koyacağınıza dair bir ipucuyla birlikte işaretler.
4. İstenen çıktıyı adlandıran **bir görev**.
5. **Sınırlar**: sayı, kaynak, alıntı veya uyum iddiası uydurmayın; yalnızca yapıştırılan materyali kullanın.
6. Bilgi eksik olduğunda **önce sormaya** ve varsayımları işaretlemeye dair bir istek.
7. **Son bir kontrol**: "List what you are unsure of" (Emin olmadığınız şeyleri listeleyin).

Bu parçaların nedenleri vardır. Yer tutucular sizi gerçek materyal getirmeye zorlar. Sınır, asistanın boşlukları uydurmayla doldurmasını engeller. Açıklayıcı soru isteği, tek seferlik bir tahmini kısa bir sohbete dönüştürür. Son satır, asistanın kendi zayıf noktalarını işaretlemesini sağlar; bu da neyi kontrol edeceğinize karar vermenize yardım eder.

### Yardımcı olan örüntüler

Rehberin `prompt-engineering` becerisi, bu rehberin kendi sözcükleriyle özetlediği teknikleri listeler:

- **İstediğiniz çıktı konusunda belirli olun**, örneğin adlandırılmış sütunları olan bir tablo veya en fazla beş maddelik numaralı bir liste; böylece asistan biçimi tahmin etmez.
- **Talimatlar belirsiz olduğunda örnekler verin**, istediğiniz örüntüyü kısa bir örnekte göstererek.
- **Asistanın bilemeyeceği bağlamı sağlayın**, örneğin terminolojiniz, kısıtlarınız ve söz konusu belge; neyi varsaymaması gerektiğini söyleyin.
- **Gerçek test vakalarına karşı yineleyin**, istemi tek bir iyi örnekle yargılamak yerine bir dizi gerçek girdi üzerinde çalıştırıp başarısız olduğu yerde gözden geçirerek.

Tek bir girdi üzerinde ayarlanmış bir istem diğerlerinde başarısız olabilir. Beceri, kısa, tuhaf ifade edilmiş veya bir alanı eksik bir girdinin, özgün örneği ele alan bir istemi bozabileceğine dikkat çeker.

### Doğrulama alışkanlıkları

Her çıktı, yanlış olmanın maliyetiyle orantılı biçimde kontrol edilmelidir. Yardımcı olan alışkanlıklar:

- **Olguları yapıştırdığınız kaynağa karşı kontrol edin.** Asistandan her ifadeyi destekleyen materyal bölümünü alıntılamasını isteyin.
- **Görmediğiniz kaynakları asla kabul etmeyin.** Önceki konuda anlatılan vakalar arasında uydurma mahkeme atıfları vardır; bunları tekrarlamayın.
- **Asistanın gördüğünü varsaydığından ayırın.** Rehberin istemleri bunu ister.
- **Hesaplamaları kendiniz sınayın** veya işlem adımlarını isteyin ve kontrol edin.
- **Ekipten dışarı çıkan her şey için ikinci bir göz kullanın**, örneğin bir müşteri yanıtı veya bir politika.
- **Önemli kullanımların kayıtlarını tutun**, Konu 6.2 — BT Hizmet Yönetiminde Yapay Zeka'da anlatıldığı gibi.

### Verileri korumak

Bir isteme bir şey yapıştırmadan önce neyi içerdiğini ve nereye gideceğini sorun. Araç ve koşulları onlar için onaylanmadıkça kişisel verileri, kimlik bilgilerini ve gizli ticari ayrıntıları kaldırın (bkz. Konu 3.13 — Bilgi Güvenliği Yönetimi). Rehberin istemleri anonimleştirmenizi ister, ancak sorumluluk sizindir. Şüpheniz varsa durumu genel terimlerle anlatın.

### Bir beceri nasıl görünür

Claude Code belgelerinden ve bu rehberdeki becerilerden, bir beceri `skills/runbook/` gibi, `SKILL.md` içeren bir dizindir. Dosya, `---` işaretleri arasında, en az bir `name` ve bir `description` içeren YAML ön bilgisiyle başlar. Belgeler, açıklamanın asistana becerinin ne yaptığını ve ne zaman kullanılacağını söylediğini belirtir ve temel kullanım durumunu başa koymayı önerir. Gövde yöntemi markdown ile verir. Başvuru belgeleri veya betikler gibi diğer dosyalar yanında durabilir ve gerektiğinde yüklenebilir; belgeler `SKILL.md`'nin kendisini kısa, 500 satırın altında tutmayı önerir.

Bu rehberdeki kopyalanmış beceriler aynı biçimi izler. Açıklamaları "Use when asked to…" ile başlar; bu da her birinin ne zaman uygulandığını netleştirir.

### Beceriler nerede yaşar

Belgeler, kişisel becerileri bir kullanıcının ana dizinindeki beceri dizininde, proje becerilerini bir deponun beceri dizininde (işlenebilir ve bir ekiple paylaşılabilir) ve eklentiler gibi diğer konumlarda anlatır. Bir ekip için sürüm kontrolü altındaki bir proje klasörü doğal yerdir: beceriler gözden geçirilir, diğer işlerle aynı süreçle değiştirilir ve herkesin kullanımına açıktır.

### Kendi ekip becerilerinizi yazmak

Bir ekip becerisi, ekibin tekrarladığı ve tutarlı biçimde yapılmasını istediği bir uygulamayı yakalar. Hizmet yönetimi için örnekler: kurum üslubunuzla bir ölüm sonrası inceleme (postmortem) nasıl yazılır, belirli bir tür bilet nasıl ön değerlendirilir, bir değişiklik talebi nasıl hazırlanır, cuma gözden geçirmeniz nasıl yürütülür. Birini yazmak için:

1. **Tekrarladığınız ve bilinen iyi bir yapılış biçimi olan bir görev seçin.**
2. **Önce açıklamayı yazın**, "Use when…" ve temel kullanım durumuyla başlayarak; böylece asistan ve meslektaşlarınız ne zaman uygulandığını bilir.
3. **Yöntemi kısa adımlar olarak yazın**, çıktı biçimi, kontroller ve kaçınılacak şeylerle birlikte.
4. **İyi bir sonucun örneklerini ekleyin**, hassas ayrıntılar kaldırılmış olarak.
5. **Neyi yapmaması gerektiğini söyleyin**, örneğin rakam uydurmak veya gözden geçirme olmadan bir şey göndermek.
6. **Gerçek vakalarda test edin** ve gözden geçirin.
7. **Ona bir sahip ve bir gözden geçirme tarihi verin**, diğer ortak belgeler gibi.

### Bu rehberdeki beceriler

Bu depodaki `skills/` klasörü, `skills/README.md` içinde listelenen skills-on-ai koleksiyonundan becerilerin kopyalarını ve bu rehber için yazılmış iki beceriyi barındırır: biri okurlar, biri bakımcılar için. Her konu, konusu için en yararlı becerilere, her birinin ne zaman kullanılacağını anlatan bir cümleyle bağlantı verir. Kopyalanan beceriler geneldir, bu rehberin içeriğine özgü değildir; bu yüzden onları başlangıç noktaları olarak kullanın ve çıktılarını kendi bağlamınıza uyarlayın.

### Sınırlar

Bu rehber için okunan hiçbir kaynak herhangi bir istem tekniğinin ne kadar iyi işlediğini ölçmez ve yapay zeka araçları hızla değişir. Okunan Claude Code belgeleri uzundu ve yalnızca kısmen okundu. Aşağıdakiler, genel kullanımda geçerliliğini koruyan pratik öğütlerdir; garanti olarak değil, sınanacak alışkanlıklar olarak sunulur.

## İyi uygulamalar

1. **Gerçek bir görevden ve gerçek materyalden başlayın.** Yapılmasına ihtiyaç duyduğunuz bir şey seçin ve olguların tanımını değil, kendilerini yapıştırın. Her yer tutucuyu somut bilgiyle doldurun.
2. **Amacı tek satırda belirtin.** Çıktının ne için olduğunu ve kimin kullanacağını söyleyin. Bu, asistanın doğru ayrıntı düzeyini seçmesine yardım eder.
3. **Çıktıyı belirtin.** İstediğiniz biçimi, uzunluğu ve yapıyı adlandırın. Karşılaştırmak istediğinizde tablo, adım istediğinizde liste isteyin.
4. **Sınırlar koyun.** Asistanın neyi yapmaması gerektiğini söyleyin: sayı, kaynak veya alıntı uydurmak; verilmeyen olguları varsaymak; metni olmadan bir kuralın uygulandığını iddia etmek.
5. **Önce açıklayıcı sorular isteyin.** Asistana yanıtlamadan önce ihtiyaç duyduğunu sormasını söyleyin. Kısaca yanıtlayın ve sonra devam etmesini isteyin.
6. **Olguları varsayımlardan ayırmasını isteyin.** Materyalinizden aldığı şeyleri ve varsaydığı şeyleri işaretletin. Bu rehberin istemleri "List what you are unsure of" ile biter.
7. **Kanıt isteyin.** Her iddiayı destekleyen materyalinizden alıntılar isteyin; böylece hızla kontrol edebilirsiniz.
8. **Yineleyin.** İlk yanıtı bir taslak olarak ele alın. Neyin yanlış olduğunu söyleyin ve bir revizyon isteyin veya istemi değiştirip yeniden deneyin.
9. **İstemleri birkaç vakada test edin.** Bir isteme güvenmeden önce, alışılmadık biri dahil üç veya dört gerçek girdi üzerinde çalıştırın. Nerede başarısız olduğunu not edin.
10. **Verileri koruyun.** Yapıştırmadan önce kişisel ve gizli ayrıntıları kaldırın. Onaylı araçları kullanın. Kurumunuzun politikasını izleyin.
11. **Kullanmadan önce kontrol edin.** Olguları, sayıları ve kaynakları doğrulayın. Müşterilere giden veya bir sistemi değiştiren her şeyi bir kişiye gözden geçirtin.
12. **İşe yarayanı paylaşın.** Yararlı olduğu görülen istemleri notlarıyla birlikte, sahibi olan, sürüm kontrolü altındaki bir ekip becerisine veya belgesine koyun.

## Ekibinizle tartışılacak sorular

**Hangi görevleri tekrarlıyoruz ki bir asistan yardımcı olabilir ve neyi kontrol etmemiz gerekir?**

Her kişiden görevleri listelemesini ve çıktı yanlış olsaydı riski işaretlemesini isteyin. Bunları düşük, orta ve yüksek risk olarak gruplayın. Düşük riskli birinden başlayın. Kolaylaştırıcı kontrol adımının ne olacağını sorabilir. Bir deneme için bir görev seçin.

**Bugün yapay zeka araçlarına neler yapıştırıyoruz ve yapmalı mıyız?**

Dürüst ve yargılamadan olun. Örnekleri listeleyin. Veri politikası ve onaylı araçlarla karşılaştırın. İnsanların yapıştırmadan önce uygulayabileceği hızlı bir kontrol üzerinde anlaşın: "Bu kişisel veri, sır veya gizli ayrıntı içeriyor mu?"

**Bu rehberin istemlerinden hangisini ilk deneriz ve hangi gerçek materyalle?**

İstemlere birlikte göz atın ve birini seçin. Yapıştırılacak gerçek materyali belirleyin, hassas ayrıntıları kaldırın ve çalıştırın. Sonuçları karşılaştırın ve istemde neyin değişeceğini tartışın. Bu, örüntüyü öğrenmenin hızlı bir yoludur.

**Bir istemin işlediğini nasıl anlarız?**

Bir test kümesi isteyin: bilinen iyi çıktıları olan birkaç gerçek girdi. Yanıtların nasıl puanlanacağını ve kimin karar vereceğini tartışın. Test kümesi olmayan bir istem bir umuttur. Bir istem için küçük bir küme üzerinde anlaşın.

**Hangi tekrarladığımız uygulama bir ekip becerisi olmayı hak ediyor?**

Adayları listeleyin: bir gözden geçirme biçimi, bir ön değerlendirme rutini, rapor şablonu. Birini seçin ve açıklamayı ve adımları birlikte taslak olarak hazırlayın. Kimin sahip olacağına ve ne zaman gözden geçirileceğine karar verin.

**Bir yapay zekanın kendi başına asla yapmasını istemeyeceğimiz şey ne?**

Eylemleri listeleyin: müşterilere göndermek, üretimi değiştirmek, erişimi onaylamak, bir önceliğe karar vermek. Nedenini tartışın. Yanıtlar, istemlerinize ve becerilerinize yazılacak sınırlardır. Kısa bir liste üzerinde anlaşın.

## Uygulamada: çevik bir ITIL örneği

Bölgesel bir hastanenin BT hizmet masasında on dört analist vardır. Masa lideri meslektaşlarının yapay zeka asistanını farklı biçimlerde kullandığını fark etmiştir: biri hasta adları dahil biletlerin tamamını herkese açık bir sohbet robotuna yapıştırır; bir diğeri ayrıntılı istemler yazar ve yararlı özetler alır; çoğu hiç kullanmaz. Bir asistanın hazırladığı yakın tarihli bir bilgi makalesi, var olmayan bir prosedür adımı içeriyordu.

Masa lideri bu rehberin yaklaşımını kullanarak bir saatlik bir oturum yapar. Verilerle başlar: grup, hiçbir araca hasta ayrıntılarının veya kimlik bilgilerinin girmeyeceği ve hastanenin uygun koşullarla lisansladığı onaylı asistanın bilet metniyle kullanılan tek araç olacağı bir kural üzerinde anlaşır. Bir görev seçer: çözülmüş bir biletten bir bilgi makalesi taslağı hazırlamak; ve bu rehberin istemlerindeki örüntüyü kullanır: tek satırlık bir amaç, anonimleştirilmiş bilet için bir yer tutucu, yalnızca biletin içeriğini kullanma, çıkarılan her adımı bir etiketle işaretleme ve emin olmadığı şeyleri listeleme talimatları. İki analist istemi beş geçmiş bilet üzerinde çalıştırır ve grup sonuçları birlikte okur. İstem bir vakada bir adım uydurur; bunun üzerine her adım için biletten bir alıntı isteyen bir satır eklerler.

Masa lideri geliştirilmiş istemi, masanın ortak klasöründe, "Use when…" ile başlayan bir açıklama, bir sahip ve bir gözden geçirme tarihiyle bir ekip becerisi olarak yazar ve taslağı hazırlanan her makalenin yayımdan önce ikinci bir analist tarafından kontrol edilmesi kuralını ekler. İki ay sonra haftada taslağı hazırlanan makale sayısı iki katına çıkmış ve gözden geçirenler öncekinden daha az hata bulmaktadır. Bazı sorunlar sürer. İki analist sıkıştığında hâlâ ayrıntıları herkese açık bir araca yapıştırmaktadır, beceri analistlerin yeniden yazdığı aşırı resmî bir ifade üretmektedir ve bir gözden geçiren göz gezdirdiğini itiraf etmektedir. Masa lideri veri kuralını her ekip toplantısında tekrarlar, beceriye bir üslup örneği ekler ve gözden geçirenlerden kısa bir kontrol listesini işaretlemelerini ister.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri asistanları kod, test ve belgeler için kullanır. Aynı alışkanlıkları uygulayın: gerçek materyal, net sınırlar, doğrulama ve gözden geçirme. Sırları istemlerin dışında tutun ve yararlı istemleri ve becerileri kodla birlikte saklayın.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri biletleri analiz etmek, çalıştırma kılavuzu taslakları hazırlamak ve gözden geçirmeler hazırlamak için istemleri kullanabilir. Kişisel verileri dışarıda tutun, çıktıları günlükler ve kayıtlarla kontrol edin ve ölüm sonrası incelemeler ve vardiya devirleri gibi ekibin tekrarladığı rutinler için beceriler yazın.

### Liderlik ve yönetişim

Liderler neyin, hangi verilerle kullanılabileceğine ve kimin hesap vereceğine dair kuralları belirler. Bir envanter, bir veri politikası ve pilotlardan kanıt isteyin. Ekiplerin istemleri ve becerileri yazıp test etmesi için zamanı destekleyin ve paylaşılan becerilerin sahipleri olduğundan emin olun.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar istemlerin ve becerilerin sonuçlarını yanıtlarda, makalelerde ve özetlerde görebilir. Sağlayıcıların bunları kontrol etmesini ve önemli olduğu yerde otomatik araçlar kullandıklarında size söylemesini bekleyin. Altta yatan materyali iyileştirmeye yardım eden hataları bildirin.

## Yaygın başarısızlık biçimleri

- **Belirsiz istekler.** Asistan tahmin yürütür. Bunun yerine materyali, amacı ve istediğiniz çıktıyı sağlayın.
- **Hassas verileri yapıştırmak.** Kişisel veya gizli ayrıntılar kurumdan çıkar. Bunun yerine onları kaldırın ve onaylı araçları kullanın.
- **Uydurma içeriği kabul etmek.** Uydurma adımlar, sayılar veya kaynaklar kullanılır. Bunun yerine sınırlar koyun, alıntı isteyin ve doğrulayın.
- **Tek örnekle ayarlama.** Bir istem bir kez işler ve başka yerde başarısız olur. Bunun yerine birkaç gerçek girdide test edin.
- **Sahipsiz beceriler.** Paylaşılan istemler eskir. Bunun yerine bir sahip ve gözden geçirme tarihi atayın ve sürüm kontrolünde tutun.
- **Kopyalanan istemlere aşırı güven.** İnternetten veya bu rehberden bir istem olduğu gibi kullanılır. Bunun yerine bağlamınıza uyarlayın ve sonuçları kontrol edin.
- **İkinci bir göz yok.** Yapay zeka çıktısı doğrudan müşterilere gider. Bunun yerine ekipten çıkan her şeyi bir kişiye gözden geçirtin.
- **Asistanı otorite saymak.** Güveni doğruluk sanılır. Bunun yerine emin olmadığı şeyleri isteyin ve kontrol edin.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| İstem pratiği | İnsanlar geçici (ad hoc) istemler yazar | Bazı insanlar istemleri paylaşır | Ekipler amaç, materyal, sınırlar ve kontrollerden oluşan ortak bir örüntü kullanır | İstem kalitesi gerçek vaka kümelerinde test edilir | İstemler paylaşılan test sonuçlarından ekipler arasında iyileştirilir |
| Beceriler | Paylaşılan beceri yoktur | Bazı kişisel beceriler vardır | Sahipleri ve gözden geçirme tarihleri olan ekip becerileri sürüm kontrolünde bulunur | Becerilerin kullanımı ve sonuçları gözden geçirilir | Beceriler ekipler ve ortaklar arasında paylaşılır ve sürdürülür |
| Doğrulama ve veri | Çıktıya güvenilir; veriler serbestçe yapıştırılır | Bazı kontroller ve veri kuralları vardır | Doğrulama alışkanlıkları ve bir veri politikası rutindir | Hatalar ve veri olayları izlenir ve buna göre harekete geçilir | Doğrulama ve veri pratiği kurum genelinde eşgüdümlenir |
| Öğrenme | Öğrenme bireyseldir | Bazı ipuçları paylaşılır | Ekipler istemleri ve becerileri iyileştirmek için düzenli oturumlar yapar | İyileştirmeler izlenir ve ölçülür | Öğrenme ekipler arasında sürekli yayılır |

## Kontrol listesi

- [ ] Ekibin hangi verilerin hangi yapay zeka araçlarına girebileceğine dair kısa bir kuralı var.
- [ ] Güvendiğimiz istemlerin belirtilmiş bir amacı, gerçek materyali, sınırları ve asistanın emin olmadığı şeyler için bir isteği var.
- [ ] Güvendiğimiz her istem en az üç gerçek girdide test edildi.
- [ ] Ekip dışına giden çıktı bir kişi tarafından gözden geçiriliyor.
- [ ] Yapay zeka çıktısındaki kaynaklar ve sayılar kaynaklara karşı kontrol ediliyor.
- [ ] Yararlı istemler, notlarıyla birlikte, sürüm kontrolü altındaki ortak bir yerde saklanıyor.
- [ ] Ekip becerilerinin net bir "Use when…" açıklaması, bir sahibi ve bir gözden geçirme tarihi var.
- [ ] Ekip, yapay zekanın kendi başına asla yapmaması gereken eylemleri listeledi.
- [ ] Personel hangi araçların onaylı olduğunu biliyor.
- [ ] İstemlerimizi ve becerilerimizi yılda en az iki kez gözden geçiriyoruz.

## Yapay zeka istemleri

**Amaç: halihazırda kullandığınız bir istemi iyileştirmek.**

```text
Here is a prompt I use: [paste it].
Here is an example of an input I give it, with sensitive details removed: [paste].
Here is what I got: [paste].
Here is what I wanted: [describe].

Diagnose why the output fell short, using only the text above. Suggest a revised prompt that: states the purpose, names the output format, sets boundaries (no invented facts, numbers, or sources), asks for clarifying questions first, requests quotes from the supplied material as evidence, and ends by asking you to list what you are unsure of. Keep placeholders in [square brackets]. Do not change the task. List what you are unsure of.
```

**Amaç: tekrarlanan bir görevi bir ekip becerisi taslağına dönüştürmek.**

```text
Help me draft a team skill in SKILL.md format for this task: [name and describe the task].

How we do it today, step by step: [paste].
What a good result looks like (an example with sensitive details removed): [paste].
What must never happen (for example inventing figures or sending without review): [list].

Write a SKILL.md with YAML frontmatter containing a name and a description that starts with "Use when" and puts the key use case first, then a body with the purpose, short method steps, output format, checks, and things to avoid. Keep it under 150 lines. Mark every item you added as an assumption. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bir istem için küçük bir test kümesi oluşturmak.**

```text
I have a prompt that [describe what it does]: [paste it].

Help me design a test set of 5 to 10 inputs: typical cases, an unusual case, a case with a missing field, and a case where the right answer is "not enough information." Tell me what to collect from real examples (with sensitive details removed), how to record the expected output, and how to score results (correct, partly correct, wrong, confidently wrong, correctly declined). Do not invent test content; give me the categories and what to look for. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: yapay zekanın yazdığı bir taslağı kaynağıyla karşılaştırarak kontrol etmek.**

```text
Here is the source material: [paste].
Here is a draft produced by an AI tool from that material: [paste].

List every statement in the draft, say whether the source supports it (quote the supporting text), contradicts it, or does not mention it, and suggest edits to remove unsupported statements. Do not add facts of your own. Give a short summary of how reliable the draft is. List what you are unsure of.
```

## Yapay zeka becerileri

- [prompt-engineering](../../../../skills/prompt-engineering/SKILL.md): güvenilir sonuçlar veren istemleri yazmak, test etmek ve iyileştirmek için kullanın.
- [machine-learning-model-card](../../../../skills/machine-learning-model-card/SKILL.md): ekibiniz bir modele dayandığında modelin ne için olduğunu ve sınırlarının neler olduğunu belgelemek için kullanın.
- [agile-coaching](../../../../skills/agile-coaching/SKILL.md): bir ekibe zaman içinde istemler ve beceriler etrafında alışkanlıklar kurmasında yardım ederken kullanın.
- [agile-itil-guide-skill](../../../../skills/agile-itil-guide-skill/SKILL.md): bu rehberdeki konuları bulmak, sorularından bir ekip sohbeti yürütmek veya istemlerinden birini uyarlamak için kullanın.
- [agile-itil-guide-maintainer-skill](../../../../skills/agile-itil-guide-maintainer-skill/SKILL.md): bu rehber için bir konu, istem veya beceri bağlantısı yazarken ya da kontrol ederken kullanın.

## Temel kaynaklar

- **Claude Code skills documentation** (code.claude.com): becerilerin bir `SKILL.md` dosyası olan dizinler olarak nasıl yapılandırıldığının açıklaması.
- **Prompt engineering** (bu rehberin `skills/prompt-engineering/SKILL.md` dosyası): tekniklerin kısa bir ifadesi ve istemlerin gerçek girdilerde test edilmesinin gerekçesi.
- **Large language model** (Wikipedia): bu sistemlerin nasıl kurulduğuna ve nerede başarısız olabileceğine dair arka plan.
- **AI Risk Management Framework** (NIST): yapay zeka risklerini yönetmek için gönüllü çerçeve; ekip politikası için yararlı.

## Kaynakça

1. Skills (Claude Code documentation) — Anthropic — https://code.claude.com/docs/en/skills
2. Large language model — Wikipedia — https://en.wikipedia.org/wiki/Large_language_model
3. Prompt engineering — Wikipedia — https://en.wikipedia.org/wiki/Prompt_engineering
4. AI Risk Management Framework — NIST — https://www.nist.gov/itl/ai-risk-management-framework
5. Hallucination (artificial intelligence) — Wikipedia — https://en.wikipedia.org/wiki/Hallucination_(artificial_intelligence)
6. Retrieval-augmented generation — Wikipedia — https://en.wikipedia.org/wiki/Retrieval-augmented_generation
7. Artificial intelligence — Wikipedia — https://en.wikipedia.org/wiki/Artificial_intelligence
8. Version control — Wikipedia — https://en.wikipedia.org/wiki/Version_control
9. Information security — Wikipedia — https://en.wikipedia.org/wiki/Information_security
