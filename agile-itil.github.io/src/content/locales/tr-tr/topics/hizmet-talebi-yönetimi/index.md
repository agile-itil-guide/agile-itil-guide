# Hizmet Talebi Yönetimi

**Hizmet talebi yönetimi, kullanıcıların erişim, ekipman ve bilgi gibi rutin isteklerini karşılar; çevik hedef, her yaygın talebi hızlı, öngörülebilir ve büyük ölçüde otomatik hale getirmektir; böylece yetenekli kişiler zamanlarını sorunlara ayırabilir.**

## Bu neden önemli

Bir hizmet masasına ulaşan işin büyük bölümü hiç de bir başarısızlık değildir. Bu, kullanıcının hizmetin sağlaması gereken bir şeyi istemesidir: yeni bir hesap, bir klasöre erişim, bir dizüstü bilgisayar, bir lisans, bir parola sıfırlama. Bu talepler öngörülebilir ve yinelidir. İyi yönetildiklerinde hızlıdırlar ve kimse fark etmez. Kötü yönetildiklerinde uzun beklemelerin, tekrarlanan soruların ve bir ekibin itibarına tek bir kesintiden daha fazla zarar veren sessiz bir hayal kırıklığının kaynağı olurlar.

Talep yönetimi, otomasyonun ve self servisin (self-service) en çok karşılığını verdiği yerdir. Her seferinde aynı adımları izleyen bir talep bir kez tasarlanabilir, sınanabilir ve büyük ölçüde otomatikleştirilebilir. [BT hizmet yönetimi hakkındaki Wikipedia maddesi](https://en.wikipedia.org/wiki/IT_service_management) hizmet talebini bir hizmete yönelik rutin istek olarak tanımlar ve rutin elle yapılan adımların yerini otomatik adımların aldığı, böylece personelin daha öncelikli işlere odaklanabildiği BT süreç otomasyonunu sayar. Bu uygulamanın amacı tek cümleyle budur.

Madde talepler hakkında bundan fazlasını söylemez. Bu nedenle bu konu, söz konusu tanımı yaygın olarak kullanılan hizmet yönetimi uygulamasından alınan pratik yönlendirmeyle, bu şekilde sunularak, ve rehberin hizmet masası, hizmet kataloğu (ITIL bunu "service catalogue" diye yazar) ve bilgi konularıyla birleştirir. Bir şey bir kaynaktan çıkan bulgu değil de yaygın bir uygulamaysa, metin bunu belirtir.

## Temel kavramlar

### Hizmet talebi nedir

**Hizmet talebi**, bir hizmetin normalde sağladığı bir şey için yapılan rutin bir istektir. Bir hizmetin aksamasını ya da aksama olasılığını ifade eden **olaydan (incident)** ve bir hizmeti değiştiren **değişiklikten (change)** farklıdır (bkz. Konu 3.2 — Olay Yönetimi ve Konu 3.4 — Değişiklik Sağlama). Sınır bulanıklaşabilir: "Finans sistemine erişim istiyorum" bir taleptir; "Erişimim var ama sistem hata gösteriyor" bir olaydır; "finans sistemine yeni bir alan ekleyin" büyük olasılıkla bir değişikliktir.

Pratik bir sınama: iş bilinen bir yordamı izliyorsa, maliyeti ve riski biliniyorsa ve "buna izin var mı?" sorusunun yanıtı önceden belirlenmişse, bu bir taleptir. Risk konusunda yeni bir yargı gerektiren her şey büyük olasılıkla bir değişiklik ya da projedir.

### Ayrımın neden önemli olduğu

Talepleri olaylarla karıştırmak ikisini de bozar. "Bilet" (ticket) sayıları iki farklı türde talebi bulanıklaştırır. Öncelikler çatışır, çünkü işi durduran bir olay bekleyebilecek bir talepten önce gelmelidir. Yanıt ölçüleri yanıltır: uzun bir ortalama kapatma süresi, olaylar hızla çözülürken taleplerin onayları beklediğini gizleyebilir. İkisini ayrı tutmak uygun hedefler belirlemenizi ve gecikmenin nerede olduğunu görmenizi sağlar (bkz. Konu 2.1 — BT Hizmet Yönetimi).

### Talep modelleri

**Talep modeli**, bir talep türü için yinelenebilir bir kalıptır: hangi bilgilerin gerektiği, kimin onaylaması gerektiği, hangi adımların kim ya da otomasyon tarafından yapıldığı ve beklenen süre. Talep modelleri hizmet yönetiminde yaygın olarak kullanılan bir fikirdir. Bir ekibe yaygın talepleri bir kez tasarlayıp çok kez çalıştırma olanağı verir. Bir hizmet kataloğu, sunulan talepleri listeler (bkz. Konu 3.8 — Hizmet Kataloğu Yönetimi).

"Yeni başlayan için dizüstü bilgisayar" modeli şunları belirtebilir: yöneticiden gereken bilgi, onay (rol standart bir listedeyse hiçbiri), adımlar (sipariş, yapılandırma, gönderim) ve beklenen süre. "Kısıtlı bir sisteme erişim" modeli ise sistem sahibinin onayını ve denetim için bir kaydı içerir.

### Onay

Bazı talepler ilerlemeden önce onay gerektirir: harcama, hassas verilere erişim ya da kıt kaynakların kullanımı. Tasarım açısından soru, onayın gerçek bir denetim katıp katmadığıdır. Her zaman evet diyen bir onay bir gecikmedir. Onay gerekli olduğunda onu hızlı ve görünür kılın, onaylayana tam olarak ne istendiğini söyleyin ve yanıt vermezse bir yedek yol tanımlayın. Onay bir role bağlıysa, örneğin bir yöneticinin ekip üyesinin talebini onaylaması gibi, rol için standart kalemleri önceden onaylamayı düşünün.

### Karşılama ve otomasyon

Karşılama (fulfillment), talebi teslim etme işidir. ITSM maddesi BT süreç otomasyonunu, personelin daha öncelikli işlere odaklanabilmesi için rutin görevlerin otomatikleştirilmesi olarak tanımlar. Otomasyon adayları sık olan, kararlı bir yordamı izleyen ve düşük risk taşıyan taleplerdir: parola sıfırlamalar, grup üyelikleri, standart yazılım kurulumları. Otomasyon, herhangi bir değişiklik kadar özenle, testlerle ve ne yaptığını görme yoluyla kurulmalıdır.

### Self servis

Pek çok kuruluş, kullanıcıların ihtiyaç duydukları hizmeti bulabildiği, hangi bilgilerin gerektiğini görebildiği ve kimseyle konuşmadan talep gönderebildiği bir portal sunar. İyi self servis, kullanıcıların kendi sözcükleriyle yazılmış net bir hizmet listesine ve açık formlara bağlıdır. Kuruluş şemasını yansıtan ve kullanıcının elinde olmayan bilgileri isteyen bir portal, insanları yeniden e-postaya ve telefona iter.

### Kurumsal hizmet yönetimi

ITSM maddesi, kurumsal hizmet yönetiminin (enterprise service management) ITSM araçlarını ve fikirlerini insan kaynakları ya da tesis yönetimi gibi diğer iş alanlarına uyguladığını belirtir. Talep yönetimi başlamak için en kolay yerdir, çünkü pek çok işlev rutin talepler alır: işe alım, seyahat, ekipman, ofis taşınmaları. Ortak bir talep platformu, her biri kendi talep modellerine ve sahiplerine sahip birkaç işleve hizmet edebilir.

### Ölçüler

Yaygın ölçüler arasında taleplerin gönderilmesinden karşılanmasına kadar ne kadar sürdüğü, talep edenin soru sormak için ne sıklıkla geri dönmesi gerektiği, kaç talebin insan emeği olmadan karşılandığı ve talep edenin memnuniyeti yer alır. Her ölçüde olduğu gibi, talepleri erken kapatmayı ödüllendiren hedeflerden kaçının. Bekleme süresine bakın, çünkü bir talebin geçen süresinin çoğu genellikle çalışmaktan değil onay ya da bilgi beklemekten oluşur (bkz. Konu 1.7 — Yalın Yazılım Geliştirme ve Konu 5.6 — Metrikler ve Ölçüm).

### Güvenlik ve uyum

Talepler çoğunlukla erişimi ve harcamayı denetler, dolayısıyla güvenlik ve denetim açısından sonuçları vardır. Kayıtlar kimin istediğini, kimin onayladığını, ne yapıldığını ve ne zaman yapıldığını göstermelidir. Erişimi artık gerekmediğinde, sonradan akla gelen bir iş olarak değil, ayrılan çalışan talep modelinin bir parçası olarak kaldırın (bkz. Konu 3.13 — Bilgi Güvenliği Yönetimi).

## İyi uygulamalar

1. **En yaygın taleplerle başlayın.** Kayıtlarınızdan hacme göre ilk on talebi listeleyin. Önce bunları tasarlayın. İyi tasarlanmış birkaç model talebin büyük bölümünü karşılar.
2. **Her biri için bir talep modeli tanımlayın.** Hangi bilgilerin gerektiğini, kimin onayladığını, adımları, her birini kimin yaptığını ve beklenen süreyi yazın. Her modeli bir sayfada tutun.
3. **Kullanıcının sözcüklerini kullanın.** Talepleri kullanıcıların adlandıracağı gibi adlandırın ("Yeni dizüstü bilgisayar edinin", "Donanım tedarik talebi türü 2" değil). Adları kullanıcılarla sınayın.
4. **Yalnızca ihtiyacınız olanı isteyin.** Bir formdaki her alanın bir amacı olmalı. Kullanıcıya sormak yerine, kullanıcının departmanı gibi bilgileri elinizdeki sistemlerden alın.
5. **Rutin olanı önceden onaylayın.** Onaylayanlarla, olaya özgü onay gerektirmeyen standart bir kalem ve rol listesi üzerinde anlaşın. Listeyi düzenli aralıklarla gözden geçirin.
6. **Gerçek onayları kolay ve hızlı yapın.** Onaylayana neyin istendiğini ve nedenini gösterin, telefondan veya e-postayla onaya izin verin ve otomatik bir hatırlatıcı ile yokluk için bir vekil belirleyin.
7. **Kararlı ve sık olanı otomatikleştirin.** Her seferinde aynı adımları izleyen ve düşük risk taşıyan talepleri seçin. Otomasyonu sınayın ve ne yaptığını kaydedin.
8. **İnsana giden bir yol bırakın.** Bir form ihtiyaçlarına uymadığında kullanıcıların yardım istemesine izin verin. Bu durumları modele ilişkin geri bildirim olarak değerlendirin.
9. **Talepleri olaylardan ve değişikliklerden ayırın.** Her birine kendi kategorisini, kuyruğunu ve ölçülerini verin. Bir talep aslında bir arıza ya da değişiklik çıktığında masanın yeniden sınıflandırmayı bilmesini sağlayın.
10. **Beklemeleri izleyin.** Yalnızca toplam süreyi değil, onay ya da bilgi beklerken geçen süreyi de ölçün. Önce azaltılacak en uzun beklemeyi seçin.
11. **Talep edenle döngüyü kapatın.** Tamamlandığını doğrulayın, işe yarayıp yaramadığını sorun ve yaramadıysa söyleyebileceği bir yol sunun. Bitti diye işaretlenmiş ama teslim edilmemiş bir talep, hâlâ açık olandan daha kötüdür.
12. **Talep kataloğunu düzenli olarak gözden geçirin.** Kimsenin yapmadığı talepleri kaldırın, neredeyse aynı olanları birleştirin ve kanıtlara dayanarak yenilerini ekleyin (bkz. Konu 3.8 — Hizmet Kataloğu Yönetimi).

## Ekibinizle tartışılacak sorular

**En sık hangi talepleri karşılıyoruz ve her biri baştan sona ne kadar sürüyor?**

Son çeyrekten ilk on talebi çıkarın ve her biri için geçen süreyi izleyin. Her talebin nerede beklediğini işaretleyin. Sürpriz genellikle sürenin çoğunun çalışma değil bekleme olmasıdır. Kimin kimi beklediğini sorun. Kolaylaştırıcı hangi talebin önce iyileştirilmesinin en kolay olacağını sorabilir.

**Taleplerimizdeki hangi onaylar hiç hayır dememiş?**

Bir onay örneklemini gözden geçirin ve reddedilenleri sayın. Hiç ret vermeyen bir onay, yararı olmayan bir gecikme olabilir. Onayın ne için olduğunu ve kimin yararına olduğunu sorun. Bazı onaylar denetim ya da hesap verebilirlik için vardır; bu meşru bir amaçtır ve onaylayana sonradan bildirim yapmak gibi daha hafif bir yolla karşılanabilir. Basitleştirmek için birini seçin.

**Kullanıcıların bize söylemek zorunda kaldığı, bizim de zaten bildiğimiz şeyler neler?**

Bir talep formuna bakın ve yanıtları başka bir sistemde bulunan alanları işaretleyin. Bu tür her alan kullanıcı için bir emek ve bir hata kaynağıdır. Bunları önceden doldurmak için ne gerektiğini sorun. Kaldırılacak ya da önceden doldurulacak bir alan seçin.

**Taleplerimizden hangileri hiçbir insan eli değmeden yapılabilir?**

Sabit bir yordamı izleyen talepleri listeleyin. Her biri için otomasyonu neyin engellediğini sorun: araçlar, erişim, hata korkusu. Otomasyonu kabul edilebilir kılacak güvenceleri, örneğin sınırları ve günlükleri, tartışın. Bir deney olarak otomatikleştirmek üzere birini seçin.

**Kullanıcılar neleri isteyebileceklerini nasıl öğreniyor?**

Birkaç kullanıcıya olağandışı bir şeyi nasıl talep edeceklerini sorun. Yanıt "tanıdığım birine sorarım" ise hizmet listesi işe yaramıyor demektir. Listenin nasıl sunulduğunu ve adların kullanıcılara anlamlı gelip gelmediğini tartışın. Bir taslağı iki ya da üç kullanıcıyla sınayın.

**Bir talep aslında başka bir şey çıktığında ne oluyor?**

Gerçekte olay ya da değişiklik olan taleplerden örnekler toplayın. Yanlış sınıflandırmanın ne kadara mal olduğunu sorun. Masanın bunu nasıl fark edip yeniden sınıflandırdığını ve talep formunun kullanıcıların doğru seçim yapmasına yardımcı olup olmadığını tartışın. Basit bir yeniden sınıflandırma adımı üzerinde anlaşın.

## Uygulamada: çevik bir ITIL örneği

Ulusal bir istatistik kurumunun 3.000 çalışanı ve 80 kişilik bir BT departmanı var. Yeni çalışanlar çalışan bir dizüstü bilgisayar ve hesaplar için olağan olarak on gün bekliyor ve yöneticiler yeni başlayanların boş oturduğundan şikâyet ediyor. Hizmet masası işe alım taleplerini tek tek biletler olarak ele alıyor; beş ekibin her biri bir adımı yapıp bileti bir sonrakine aktarıyor.

Bir iyileştirme lideri bir işe alım talebinin haritasını çıkarıyor. Gerçek işin yaklaşık üç saat sürdüğünü, gerisinin beklemek olduğunu görüyor: yöneticinin ayrıntıları vermesini, standart bir dizüstü bilgisayar için bütçe onayını ve her ekibin biletin farkına varmasını beklemek. Ekip, yeni başlayanlar için bir talep modeli tasarlıyor. Yönetici, başlangıç tarihinden üç hafta önce kısa bir form dolduruyor ve alanların çoğu insan kaynakları sisteminden doldurulmuş geliyor. Rol için standart dizüstü bilgisayarlar ve hesaplar önceden onaylanmış. Bir betik hesapları ve grupları oluşturuyor; donanım bir stok listesinden otomatik olarak sipariş ediliyor; masa tek bir görev listesi alıyor. Yeni başlayanın yöneticisi güncellemeler ve bir onay alıyor.

İki ay sonra, form zamanında gönderildiğinde talepten hazır dizüstü bilgisayara kadar geçen medyan süre üç güne düşüyor. Bazı zorluklar sürüyor. Yöneticilerin yaklaşık üçte biri formu hâlâ geç gönderiyor, dolayısıyla yeni başlayanlar hâlâ bekliyor ve insan kaynakları kaydında departman kodu eksik olduğunda betik başarısız oluyor, bu da elle onarım işi doğuruyor. Ekip insan kaynakları işe alım kontrol listesine bir hatırlatıcı ekliyor, başarısız betikler için bir uyarı kuruyor ve verilerin iyileştirilmesi için insan kaynaklarıyla konuşmaya başlıyor. Ayrıca standart listeye uymayan roller için insana giden bir yol da bırakıyorlar.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri çoğunlukla gerçekte değişiklik olan talepler alır: yeni bir alan, yeni bir rapor. Masanın bunları tanımasına ve ürün biriktirme listenize yönlendirmesine yardımcı olun. Hizmetiniz için erişim gibi talepler sıksa, net sınırları ve günlüğü olan bir self servis yolu kurun.

### Hizmet ve operasyon ekipleri

Operasyon ve masa, talep modellerinin çoğuna sahiptir. Önce yaygın olanları tasarlayın, beklemeyi kaldırın ve güvenli olduğu yerde otomatikleştirin. Model kurmak ve gözden geçirmek için zaman ayırın, çünkü talep işi iyileştirme işini kolayca dışarı iter. Beklemelere ilişkin verileri onaylayanlar ve yöneticilerle paylaşın.

### Liderlik ve yönetişim

Liderler ve onaylayanlar beklemenin büyük bölümünü şekillendirir. Hangi onayların denetim, hangilerinin gecikme kattığını sorun ve risk düşük olduğunda önceden onaylamayı kabul edin. İşlevler arasında ortak bir talep platformunu destekleyin ve bilet sayıları yerine bekleme süresi ölçüleri isteyin.

### Müşteriler ve kullanıcılar

Kullanıcılar net adlardan, kısa formlardan ve dürüst tahminlerden yarar sağlar. İstekte bulunurken eksiksiz bilgi verin ve acil olduğunda bunu ve nedenini söyleyin. Bir talep ihtiyacınızı karşılamadığında ekibe bildirin, çünkü bu bir sonraki kişi için modeli iyileştirir.

## Yaygın başarısızlık biçimleri

- **Talepleri olay gibi ya da tersi biçimde ele almak.** Öncelikler ve raporlar bozulur. Bunun yerine ikisini ayırın ve yeniden sınıflandırmayı öğretin.
- **Çok şey soran formlar.** Kullanıcılar portalı bırakır. Bunun yerine yalnızca ihtiyacınız olanı isteyin ve gerisini önceden doldurun.
- **Tören olarak onaylar.** Her talep hiç ret vermeyen bir imzayı bekler. Bunun yerine rutin kalemleri önceden onaylayın ve gerçek onayları hızlı tutun.
- **Güvencesiz otomasyon.** Bir betik büyük ölçekte yanlış değişiklik yapar. Bunun yerine otomasyonu sınayın, sınırlayın, günlüğe kaydedin ve başarısızlıkları izleyin.
- **İç adlar.** Kullanıcılar ihtiyaç duyduklarını bulamaz. Bunun yerine talepleri kullanıcıların sözcükleriyle adlandırın ve sınayın.
- **İnsana giden yolun olmaması.** Olağandışı ihtiyaçlar kaybolur. Bunun yerine yardım sunun ve alışılmadık talepleri geri bildirim olarak değerlendirin.
- **Yalnızca hızı saymak.** Talepler erken kapatılır. Bunun yerine talep edenle doğrulayın ve yinelenen talepleri izleyin.
- **Talepleri hiç emekliye ayırmamak.** Liste bayatlar. Bunun yerine kullanımı düzenli olarak gözden geçirin ve kimsenin istemediklerini kaldırın.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Talep modelleri | Her talep ad hoc ele alınır | Bazı sık taleplerin modelleri vardır | En sık taleplerin modelleri sahipleri ve beklenen sürelerle birlikte vardır | Model performansı ölçülür ve ayarlanır | Modeller işlevler ve tedarikçiler arasında paylaşılır |
| Onay | Onay gayriresmi ya da alışkanlıkla verilir | Bazı rutin kalemler önceden onaylıdır | Önceden onay listeleri ve hızlı onay yolları standarttır | Onay sonuçları ve beklemeler gözden geçirilir | Onay kuralları, risk verilerine dayanarak işlevler arasında uyumlu hale getirilir |
| Otomasyon ve self servis | Talepler e-postayla elle ele alınır | Bazı talepler bir portalda sunulur ya da otomatiktir | Sık ve düşük riskli talepler otomatiktir, self servis standarttır | Otomasyon başarısı ve kullanıcı emeği ölçülür | Otomasyon ve self servis BT, İK ve tesis yönetimini kapsar |
| Öğrenme ve iyileştirme | Talepler çözümlenmez | Bazı sayımlar toplanır | Beklemeler ve yinelenen talepler düzenli olarak gözden geçirilir | İyileştirmeler verilerden planlanır ve etkileri denetlenir | İyileştirme fikirleri kuruluş genelindeki kullanıcılardan ve ekiplerden gelir |

## Kontrol listesi

- [ ] En yaygın on talebimizi ve her birinin ne kadar sürdüğünü biliyoruz.
- [ ] Her birinin bir talep modeli var: gereken bilgi, onaylayan, adımlar, sahip, beklenen süre.
- [ ] Talepler kullanıcıların sözcükleriyle adlandırılmıştır.
- [ ] Formlar yalnızca gerekli bilgiyi ister ve bildiklerimizi önceden doldurur.
- [ ] Rutin kalemler önceden onaylıdır; gerçek onayların hızlı bir yolu ve bir vekili vardır.
- [ ] Sık ve düşük riskli talepler testler ve günlüklerle otomatikleştirilmiştir.
- [ ] Talepler, olaylar ve değişiklikler bir yeniden sınıflandırma adımıyla ayrılmıştır.
- [ ] Toplam süreyle birlikte bekleme süresini de ölçüyoruz.
- [ ] Talep edenlerden tamamlandığını doğrulamaları istenir.
- [ ] Talep listesi yılda en az iki kez gözden geçirilir.

## Yapay zeka istemleri

**Amaç: en yaygın talepleri ve en uzun beklemeleri bulmak.**

```text
Here is data on service requests from the last [period]: [paste a table with request type, date submitted, date approved if any, date fulfilled, and any notes; remove personal data].

Using only my data, list the ten most common request types with counts, the typical elapsed time for each (give the middle value and the range), and how much of that time was waiting for approval, if the data shows it. Highlight the three requests with the longest waits. Suggest questions to ask the owners. Do not invent numbers or causes. If the data is too thin, tell me what to collect. List what you are unsure of.
```

**Amaç: tek bir talep için talep modeli yazmak.**

```text
Help me write a request model for [request, e.g. "access to a shared team folder"].

How it is handled today, step by step, with who does each: [paste].
Information the requester must provide today: [list].
Approvals today and who gives them: [list].
Rules we must follow, with source text if available: [paste, or write "none known"].

Produce a one-page model: purpose, who may request, information needed (mark what could be prefilled from existing systems), approval (and a suggestion for pre-approval where low risk), steps with who or what does each, expected time marked as [to be agreed], and how completion is confirmed. Mark assumptions. Do not invent rules. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bir talep formunu daha kısa ve daha net olacak biçimde yeniden yazmak.**

```text
Here is a request form we use: [paste the fields and instructions].
Here is what we already know about the requester from other systems: [list, such as name, department, manager].

For each field, say whether it is needed, could be prefilled, or could be removed, and give a reason from the text. Rewrite the form with clear labels in plain language. Do not remove any field that I have marked as required by a rule: [list, or write "none known"]. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: önce neyin otomatikleştirileceğine karar vermek.**

```text
Here is a list of our requests with volume per month, steps, and how risky each step is (my judgment): [paste].
Tools we can automate with: [list, or write "unknown"].
Safeguards we can put in place: [list, such as logs, limits, approvals for exceptions].

Rank the requests as automation candidates, using only my data, and explain each ranking in one sentence. For the top two, list what could go wrong and a safeguard for each. Do not invent volumes. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Yapay zeka becerileri

- [service-catalog](../../../../skills/service-catalog/SKILL.md): kullanıcıların yapabileceği talepleri, kendi sözcükleriyle ve sahipleriyle birlikte listelemek için kullanın.
- [demand-analysis](../../../../skills/demand-analysis/SKILL.md): en yaygın talepleri ve hacimlerini bulmak için kullanın.
- [workflow-analysis](../../../../skills/workflow-analysis/SKILL.md): bir talepteki adımları ve beklemeleri çözümlemek için kullanın.
- [user-story](../../../../skills/user-story/SKILL.md): bir talebi kabul ölçütleriyle birlikte kullanıcının bakış açısından tanımlamak için kullanın.
- [runbook](../../../../skills/runbook/SKILL.md): elle yapılmaya devam eden talepler için adımları belgelemek için kullanın.

## Temel kaynaklar

- **IT service management** (Wikipedia): hizmet talebini, kurumsal hizmet yönetimini ve BT süreç otomasyonunu tanımlar.
- **Help desk** (Wikipedia): bir masaya ulaşan talepler için kuyruk yönetimi ve yönlendirme konusunda arka plan.
- **Business process automation** (Wikipedia): rutin işin otomatikleştirilmesi üzerine genel arka plan.
- **ITIL** (Wikipedia): ITIL'de hizmet talebi yönetiminin bağlamı.

## Kaynakça

1. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
2. Help desk — Wikipedia — https://en.wikipedia.org/wiki/Help_desk
3. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
4. Enterprise service management — Wikipedia — https://en.wikipedia.org/wiki/Enterprise_service_management
5. Business process automation — Wikipedia — https://en.wikipedia.org/wiki/Business_process_automation
6. Self-service software — Wikipedia — https://en.wikipedia.org/wiki/Self-service_software
7. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
8. Access control — Wikipedia — https://en.wikipedia.org/wiki/Access_control
