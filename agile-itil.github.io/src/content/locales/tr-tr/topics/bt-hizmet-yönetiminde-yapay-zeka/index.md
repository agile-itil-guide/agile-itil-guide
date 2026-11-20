# BT Hizmet Yönetiminde Yapay Zeka

**Yapay zeka, BT hizmet yönetiminde tespiti, ön değerlendirmeyi (triage) ve bilgi işini hızlandırabilir; ancak yalnızca bir kişinin hesap verebilir kaldığı, yanıtların kendi materyalinize dayandırıldığı ve hata, yanlılık ve veri ifşası risklerinin yönetildiği yerlerde kullanımı güvenlidir.**

## Bu neden önemli

Hizmet yönetimi çok miktarda dil ve örüntü tanıma içerir: biletleri okumak, olayları özetlemek, bilgi aramak, yanıt taslağı hazırlamak, izleme verilerindeki olağandışı sinyalleri fark etmek. Bunlar, son dönem yapay zeka sistemlerinin en yetenekli göründüğü görevlerdir ve satıcılar bunları hizmet masalarına ve operasyon araçlarına eklemek için acele etmiştir. Ekiplere, daha önce sorulmadıysa, bunları kullanıp kullanmayacakları sorulacaktır.

Fırsat gerçektir ve tehlikeler de öyle. Yapay zeka sistemleri yanlışları güvenle ifade edebilir, eğitimlerindeki ve kendilerine verilen verilerdeki yanlılıkları yansıtabilir, dikkatsizce beslenirse gizli bilgileri ifşa edebilir ve insanları kontrol etmedikleri çıktıya güvenmeye yöneltebilir. Yaygın biçimde bildirilen birkaç vaka, yersiz güvenin maliyetini göstermektedir. Yapay zekayı düşünmeden benimseyen bir hizmet kuruluşu müşterilerine ve kendi itibarına zarar verebilir.

2026'ya gelindiğinde yapay zeka çerçevenin içine de girmiştir. PeopleCert'in herkese açık sertifikasyon sayfası yeni ITIL'i "Practical and AI-native by design" (Pratik ve tasarımı gereği yapay zeka yerlisi) olarak tanımlar ve yapay zekanın "sorumlu biçimde ve ölçekte" yönetilmesini kapsayan bir ITIL AI Governance (Version 5) modülünü listeler (bkz. Konu 2.2 — ITIL). Bu rehber, sahibinin yayınlarından ITIL 5'in yapay zeka hakkında ayrıntılı olarak ne söylediğini doğrulayamamıştır; bu nedenle bu konu çerçevenin tutumunu bu ifadelerin ötesinde anlatmaz. AIOps ve yapay zeka halüsinasyonu hakkındaki Wikipedia maddelerinden, NIST'in AI Risk Management Framework sayfasından ve pratik akıl yürütmeden yararlanır ve uygulamayı bu şekilde etiketler.

## Temel kavramlar

### Yapay zekanın hizmet yönetiminde yardımcı olduğu yerler

Kullanımların çoğu birkaç gruba girer. Tablo, örnekleri ve her birinin taşıdığı risk türünü, bu rehberin okumasıyla gösterir.

| Kullanım | Yapay zekanın yaptığı | Ana riskler |
|---|---|---|
| **Tespit ve ilişkilendirme (AIOps)** | Anormallikleri bulur, ilişkili etkinlikleri gruplar, olası nedenleri önerir | Yanlış alarmlar, kaçırılan etkinlikler, opak akıl yürütme |
| **Hizmet masası yardımı** | Yanıtlar önerir, biletleri özetler, yanıt taslağı hazırlar, talepleri yönlendirir | Yanlış veya uydurma yanıtlar, üslup, gizlilik |
| **Bilgi işi** | Makaleleri taslak olarak hazırlar ve iyileştirir, bilgi arar | Uydurma içerik, eskimiş kaynaklar |
| **Olay ve sorun analizi** | Zaman çizelgelerini özetler, hipotezler önerir, inceleme taslakları hazırlar | Makul görünen ama dayanaksız nedenler |
| **Değişiklik ve sürüm desteği** | Değişiklikleri gözden geçirir, not taslakları hazırlar, risk önerir | Aşırı özgüven, kaçırılan bağlam |
| **Kod ve otomasyon** | Betikler ve yapılandırma yazar | Güvensiz veya yanlış kod, gizli bağımlılıklar |
| **Analiz ve raporlama** | Verileri özetler, rapor taslakları hazırlar | Yanlış hesaplamalar, uydurma rakamlar |

### AIOps

Wikipedia maddesi AIOps'u, veri merkezi yönetimini otomatikleştirmek ve iyileştirmek için yapay zeka, makine öğrenimi ve büyük veri analitiğinin kullanılması olarak tanımlar; amaç BT sorunlarını geleneksel yöntemlerden daha verimli biçimde tespit etmek, teşhis etmek ve çözmektir. Gartner'ın AIOps'u ilk kez 2016'da tanımladığını söyler. Madde etkinlik ilişkilendirme, anormallik tespiti, kök neden analizi, nedensellik belirleme, öngörücü analitik, olay yönetimi, otomatik iyileştirme, performans tahmini, kaynak tahsisi ve kapasite yönetimi gibi yetenekleri listeler. AIOps'un günlükler ve izleme gibi gözlemsel verilerden, biletler, etkinlikler ve olay kayıtları gibi etkileşim verilerinden yararlandığını söyler.

Madde, ortalama tespit süresinin yüzde 15 ila 20 iyileşmesi ve kritik olayların yüzde 50'nin üzerinde azalması gibi yararlar iddia eder, ancak bunların tek bir danışmanlık makalesinden geldiğini ve metinde bağımsız olarak doğrulanmadığını not eder. Hiçbir eleştiri, başarısızlık vakası veya sınırlama belirtmez. Satıcı iddialarına buna göre yaklaşın ve her aracı kendi olaylarınızla sınayın (bkz. Konu 3.10 — İzleme ve Etkinlik Yönetimi).

### Üretken yapay zeka ve halüsinasyon

Yapay zekada halüsinasyon hakkındaki Wikipedia maddesi onu, olgu olarak sunulan yanlış veya yanıltıcı bilgi içeren bir yanıt olarak tanımlar ve terimin yazılımı insan biçimli göstermesi nedeniyle eleştirildiğini not eder. Nedenleri verir: bir sonraki sözcüğü tahmin etmeye yönelik ön eğitim, model bilgiden yoksun olduğunda tahmin yürütmeyi ödüllendirir, veri kümeleri eksik veya temsil gücü zayıf olabilir ve OpenAI araştırmacıları eğitimin ve değerlendirmenin belirsizliği kabul etmek yerine tahmin yürütmeyi ödüllendirdiğini savunur. Kaydettiği örnekler şunlardır:

- **Mata v. Avianca (Mayıs 2023):** bir avukat ChatGPT'nin ürettiği altı sahte dava sundu; hâkim 23 Haziran 2023'te 5.000 ABD doları para cezası verdi.
- **Moffatt v. Air Canada (Şubat 2024):** bir mahkeme, bir havayolunu sohbet robotunun uydurduğu bir cenaze indirimi politikasına bağlı tuttu.
- Yanlış atıflar içeren bir danışmanlık şirketinin raporları ve 178 GPT-3 kaynağından 69'unun yanlış veya var olmayan tanımlayıcılara sahip olduğunu bulan bir çalışma.

Bunlar doğrulanmamış çıktıya güvenmenin sonuçlarıdır: hukuki sorumluluk, mali maruziyet ve zedelenmiş güven. Hizmet yönetiminde, bir politika veya prosedür uyduran bir sohbet robotu aynı sınıftan bir risk yaratır.

### Azaltma: dayandırma ve kontroller

Madde, geri getirme destekli üretimi (retrieval-augmented generation, RAG), modelin yanıtlamadan önce dış kaynaklara erişmesine izin vermek olarak tanımlar. Ayrıca veriyle ilgili yöntemleri, model ve çıkarım yöntemlerini ve korkuluk yazılımı ile güven puanlaması gibi önerileri listeler ve verdiği hiçbir kaynağın bunlardan herhangi birinin halüsinasyonu ne kadar azalttığını nicelleştirmediğini not eder. Bir hizmet ekibi için pratik azaltma yolları şunlardır:

- **Yanıtları kendi onaylı materyalinize dayandırın**, örneğin bilgi tabanına, ve kaynağı gösterin.
- Bir müşteriyi, bir taahhüdü veya üretimi etkileyen her şey için **bir kişiyi döngüde tutun**.
- **Yapay zekanın emin olmadığı şeyleri sorun** ve desteklenmeyen ifadeleri doğrulanmamış sayın.
- Doğru yanıtın "bilmiyorum" olduğu vakalar dahil gerçek vakalar üzerinde **düzenli olarak test edin**.

### Risk yönetimi çerçeveleri

ABD Ulusal Standartlar ve Teknoloji Enstitüsü (NIST), gönüllü kullanım için tasarlandığını, yapay zekanın bireyler, kuruluşlar ve toplum için risklerini yönetmeye ve yapay zeka ürünlerinin, hizmetlerinin ve sistemlerinin tasarımına, geliştirilmesine, kullanımına ve değerlendirilmesine güvenilirlik hususlarını dahil etme yeteneğini iyileştirmeye yardımcı olmayı amaçladığını söylediği AI Risk Management Framework'ü (AI RMF 1.0) 26 Ocak 2023'te yayımlamıştır. NIST'in sayfası dört işlevi adlandırır: Govern, Map, Measure ve Manage; ancak bunları açıklamaz. Ayrıca kuruluşların üretken yapay zekaya özgü riskleri belirlemesine yardımcı olmak için 26 Temmuz 2024'te bir Generative Artificial Intelligence Profile (NIST-AI-600-1) yayımlamış ve çerçevenin gözden geçirilmekte olduğunu söylemiştir. Ayrıntı için çerçevenin kendisini okuyun. Yasalar ve standartlar gibi yapay zekaya ilişkin diğer kurallar ülkeye ve sektöre göre farklılık gösterir; hukuk ve uyum işlevlerinize sorun ve metni edinin (bkz. Konu 5.7 — Yönetişim, Risk ve Uyum).

### Veri koruma ve gizlilik

Bir yapay zeka hizmetine verilen her şey, hizmete ve koşullara bağlı olarak saklanabilir, eğitim için kullanılabilir veya ifşa edilebilir. Biletler, günlükler ve sohbet dökümleri çoğunlukla kişisel veriler, kimlik bilgileri ve gizli iş bilgileri içerir. Herhangi bir yapay zeka aracını gerçek verilerle kullanmadan önce verinin nereye gittiğini, kimin görebildiğini, ne kadar süre saklandığını ve modelleri eğitmek için kullanılıp kullanılmadığını öğrenin ve bilgi güvenliği politikanızı uygulayın (bkz. Konu 3.13 — Bilgi Güvenliği Yönetimi). Onaylamadığınız bir araca yapıştırmadan önce kişisel ve gizli verileri kaldırın veya değiştirin.

### Hesap verebilirlik ve şeffaflık

Yapay zekanın katkıda bulunduğu kararlar için bir kişi veya bir ekip hesap verebilir kalmalıdır. Yapay zeka bir yanıt taslağı hazırladığında gönderen sorumludur. Yapay zeka bir kök neden önerdiğinde araştırmacı onu sınamaktan sorumludur. Yasa, sözleşme veya adalet gerektirdiğinde, müşterilere otomatik bir sistemle konuştuklarını söyleyin ve bir kişiye giden bir yol verin. Önemli kararlar için, diğer araçlarda yaptığınız gibi, yapay zekaya ne sorulduğunun ve neyi ürettiğinin kayıtlarını tutun (kanıt için bkz. Konu 5.1 — Çevik Hizmet Yönetimi).

### Yanlılık ve adalet

Yapay zeka sistemleri geçmiş kararları ve boşlukları yansıtan verilerden öğrenir. Geçmiş biletlerle eğitilmiş bir ön değerlendirme asistanı, bazı kullanıcı gruplarına veya bazı sorun türlerine daha düşük öncelik verebilir. Çıktıları gruplar arasında kontrol edin, testlere farklı bakış açılarından insanları dahil edin ve örüntülere dikkat edin. Bu rehber için okunan kaynaklar yanlılığı ayrıntılandırmaz; dolayısıyla bu bir bulgu değil, genel bir uyarıdır.

### Yapay zekayı ölçmek

Herhangi bir yapay zeka adımının yalnızca hacmini değil, kalitesini ve etkisini ölçün: insanların onu ne sıklıkla geçersiz kıldığı, ne sıklıkla yanlış olduğu, görevlerin onunla ve onsuz ne kadar sürdüğü ve kullanıcıların ne söylediği (bkz. Konu 5.6 — Metrikler ve Ölçüm). Satıcı rakamlarına karşı temkinli olun; AIOps maddesinin kendi yarar iddiaları tek bir kaynağa dayanır.

### Beceriler ve istemler

Yapay zekayla çalışmanın pratik becerisi net talimatlar yazmayı, doğru materyali sağlamayı, belirsizliği sormayı ve çıktıyı doğrulamayı içerir. Konu 6.3 — Yapay Zeka Becerileri ve İstemleri bunu ayrıntılı olarak ele alır.

### Kaynakların sınırları

AIOps maddesi hiçbir eleştiri içermez ve yarar rakamları tek bir kaynaktan gelir; halüsinasyon maddesi güncelleme gerektiren olarak işaretlenmiştir ve kısmen okunmuştur; NIST'in sayfası çerçevenin işlevlerini açıklamaz; ve PeopleCert'in sayfası ITIL 5'in yapay zeka hakkında ne söylediğini açıklamaz. Bu nedenle bu konu temkinli bir anlatım sunar ve ayrıntıları birincil kaynaklara bırakır.

## İyi uygulamalar

1. **Düşük riskli bir kullanım ve net bir soruyla başlayın.** Hataların ucuz ve yakalanması kolay olduğu bir görev seçin, örneğin iç kullanım için bir özet taslağı hazırlamak, ve başarının ne anlama geldiğini tanımlayın.
2. **Bir kişiyi hesap verebilir tutun.** Yapay zekanın katkıda bulunduğu şeylerden kimin sorumlu olduğunu belirleyin ve bir müşteriye ulaşan, üretimi değiştiren veya taahhütte bulunan her şey için gözden geçirme isteyin.
3. **Yanıtları onaylı materyale dayandırın.** Yanıtlar için yapay zeka kullandığınız yerde onu kendi bilgi tabanınıza bağlayın ve kaynağı gösterin. Bir kaynağı olmadığında "bilmiyorum" demesini sağlayın.
4. **Verileri koruyun.** Hangi verinin hangi araca gidebileceğine karar verin, kişisel ve gizli verileri kaldırın ve koşullarını okuduğunuz onaylı araçları kullanın. Güvenlik ve hukuk personelini erkenden dahil edin.
5. **Gerçek vakalarla test edin.** Yanıtları bilinen gerçek biletlerden ve olaylardan oluşan bir küme toplayın, yapay zekayı bunlar üzerinde çalıştırın ve nerede başarısız olduğunu kaydedin. Araç veya ayarlar her değiştiğinde tekrarlayın.
6. **İddiaları ve kaynakları doğrulayın.** Uydurma mahkeme atıfları vakalarının gösterdiği gibi isimleri, sayıları, atıfları ve prosedürleri kaynaklara karşı kontrol edin. Görmediğiniz kaynakları asla kabul etmeyin.
7. **Müşterilere dürüst olun.** Önemli olduğu yerde otomatik bir sistemin yanıt verdiğini söyleyin ve bir kişiye kolay bir yol verin.
8. **Yanlılığa dikkat edin.** Çıktıları kullanıcı grupları ve sorun türleri arasında gözden geçirin ve boşlukları fark edebilecek insanları dahil edin. Zarar görülen yerde kullanımı ayarlayın veya durdurun.
9. **Kaliteyi ve etkiyi ölçün.** Geçersiz kılma oranlarını, hata oranlarını, kazanılan zamanı ve kullanıcı görüşlerini izleyin. Yapay zekasız süreçle karşılaştırın ve satıcı rakamlarına kuşkuyla yaklaşın.
10. **Kayıt tutun.** Önemli kararlar için neyin sorulduğunu ve üretildiğini, kimin gözden geçirdiğini ve neye karar verildiğini saklayın. Bu hesap verebilirliği ve denetimi destekler.
11. **Bir risk çerçevesi kullanın.** Yapay zekanın nerede serbest olduğuna dair kararları yapılandırmak için NIST'in AI RMF'si veya kurumsal bir yapay zeka politikası gibi tanınmış bir yaklaşım benimseyin. Bunu bir düşünme rehberi olarak ele alın.
12. **İnsanları eğitin.** Personele araçların nasıl çalıştığını, nerede başarısız olduğunu ve nelere izin verildiğini öğretin. Araçlar ve kurallar değiştikçe eğitimi güncelleyin.

## Ekibinizle tartışılacak sorular

**Yapay zekayı resmî olarak veya değil, şu anda nerelerde kullanıyoruz?**

Dürüstçe sorun. Personel çoğunlukla gerçek biletlerle herkese açık araçlar kullanır. Amaç cezalandırmak değil, anlamaktır. Kullanımları ve ilgili verileri listeleyin. Hangilerinin kabul edilebilir olduğunu ve hangilerinin daha güvenli bir yol gerektirdiğini tartışın. Kısa bir politika üzerinde anlaşın.

**En çok hangi görevde yardım isterdik ve yapay zeka yanlış yaparsa ne olur?**

Bir görev seçin ve başarısızlık durumunu baştan sona izleyin. Yanıt bir özür e-postasıysa risk küçüktür; bir müşteriye yanlış bir talimatsa risk daha yüksektir. Bu, kullanımları riske göre sıralamaya yardım eder. Sınırlı zararı olan bir ilk pilot seçin.

**Bir yapay zeka yanıtının yanlış olduğunu nasıl anlarız?**

Yanıtları kimin ve nasıl kontrol ettiğini sorun. Yaygın yanıtlar: kimse veya soran kişi. Kaynakları, testleri ve ikinci gözden geçirmeleri tartışın. Her kullanım türü için asgari bir kontrol üzerinde anlaşın.

**Bir yapay zeka aracına hangi verileri koymaktan rahatız ve hangilerinden değiliz?**

Türleri toplayın: biletler, günlükler, müşteri adları, kimlik bilgileri, sözleşmeler. Her birini kabul edilebilir, hassas kısımlar kaldırıldıktan sonra kabul edilebilir veya asla olarak işaretleyin. Güvenlik ve hukukla kontrol edin. Tek sayfalık bir rehber olarak yazın.

**Yapay zeka destekli bir karar ters gittiğinde kim hesap verir?**

Araç destekli bir kararın geçmiş bir örneğini kullanın. Kimin yanıt verdiğini sorun. Adı belli bir kişinin hesap verebilir kaldığı ve hangi kanıtı saklaması gerektiği üzerinde anlaşın. Kimsenin hesap vermeyeceği herhangi bir boşluğu not edin.

**Bir aracın tutulmaya değer olduğuna bizi ne ikna ederdi?**

Ekipten kabul edecekleri kanıtı tarif etmesini isteyin: eşit veya daha iyi kaliteyle kazanılan zaman, daha az hata, kullanıcı memnuniyeti. Bunu bir denemede nasıl toplayacağınızı tartışın. Bir gözden geçirme tarihi üzerinde anlaşın.

## Uygulamada: çevik bir ITIL örneği

Ulusal bir vergi idaresinin BT hizmet masası, personelden haftada yaklaşık 1.200 temas alır ve bunların çoğu rutin sorulardır. Masa yöneticisi, bilgi tabanından yanıtlar öneren ve yanıt taslakları hazırlayan bir yapay zeka asistanı önerir. İdarenin güvenlik görevlisi biletlerdeki kişisel veriler ve personele ulaşan yanlış yanıtlar konusunda kaygılıdır.

Sınırlı bir pilot üzerinde anlaşırlar. Asistan yalnızca onaylı bilgi makalelerinden çalışır, her önerinin hangi makaleden geldiğini gösterir ve ilgili bir şey bulamadığında bunu söyler. Analistler gönderilmeden önce önerilen her yanıtı gözden geçirir ve araç kendi başına gönderemez. Biletler kişisel veriler ve kimlik bilgileri için taranır ve bunlar asistan görmeden önce kaldırılır. Pilottan önce yanıtları bilinen 200 geçmiş biletten oluşan bir test kümesi kullanılır ve ekip asistanın nerede başarısız olduğunu kaydeder. Masa yöneticisi ve güvenlik görevlisi ölçümler üzerinde anlaşır: analistlerin önerileri ne sıklıkla düzenlediği veya reddettiği, ilk yanıt süresi ve personele yönelik kısa bir memnuniyet sorusu. Pilot üç ay sürer ve yönetici, bir analist ve bir personel temsilcisini içeren ortak bir gözden geçirmeye rapor verir.

Sonunda analistler yaygın sorular için önerilerin çoğunu kabul eder ve bunlar için yanıt süresi düşer. Test kümesi, asistanın yakın zamanda değişen bir politikaya dair sorularda, bilgi makalesi güncel olmadığı için, kendinden emin ama yanlış bir yanıt verdiğini gösterir. Bazı sorunlar sürer. İki analist meşgulken önerileri az kontrolle göndermeye başlamıştır, standart olmayan bir soru soran bir personele konuyu kaçıran sıradan bir yanıt gitmiştir ve satıcının veri saklamaya ilişkin koşulları belirsizdir. Yönetici, politika değişikliklerinin yürürlüğe girmeden önce bilgi makalesini güncellemesi gerektiğine dair bir kural ekler, gönderilen yanıtların kıdemli bir analist tarafından örneklem kontrolünü kullanır ve pilotu genişletmeden önce satın alma birimi ile güvenlik görevlisinden koşulları netleştirmesini ister.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri ürünlere yapay zeka özellikleri ekleyebilir ve kod ve test yazmak için yapay zeka kullanabilir. Üretilen kodun doğruluğunu ve güvenliğini kontrol edin, sırları istemlerin dışında tutun ve yapay zekanın devrede olduğu konusunda kullanıcılara açık olun. Hizmetinize yapay zeka davranışı için izleme yerleştirin.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri yapay zekayla izlemede, masa araçlarında ve analizde karşılaşır. Yapay zeka önerilerini hipotez olarak ele alın, sınayın ve kayıt tutun. Hangi verilerin kullanılabileceğini tanımlamaya yardım edin ve dayandırma materyalini iyileştirmek için geri bildirim verin.

### Liderlik ve yönetişim

Liderler yapay zeka için politikayı, risk iştahını ve hesap verebilirliği belirler. Satıcı iddiaları değil, bir kullanım envanteri, bir risk çerçevesi ve pilotlardan kanıt isteyin. Hukuk, güvenlik ve gizlilik personelinin en baştan dahil olduğundan emin olun.

### Müşteriler ve kullanıcılar

Müşterilere ve kullanıcılara, önemli olduğu yerde otomatik bir sistemle muhatap olduklarında bunun söylenmesi ve bir kişiye giden bir yol verilmesi gerekir. Yanlış veya garip yanıtları bildirin, çünkü bunlar kanıttır. Sağlayıcılara verilerinizi nasıl koruduklarını ve yapay zeka çıktısını nasıl kontrol ettiklerini sorun.

## Yaygın başarısızlık biçimleri

- **Doğrulanmamış çıktıya güvenmek.** Uydurma olgular müşterilere ulaşır. Bunun yerine yanıtları onaylı materyale dayandırın ve göndermeden önce doğrulayın.
- **Gölge yapay zeka.** Personel gerçek verileri herkese açık araçlara yapıştırır. Bunun yerine onaylı araçlar ve net bir veri politikası sağlayın.
- **Hesap verebilir kişi yok.** Yapay zeka destekli kararların hesabını kimse vermez. Bunun yerine bir sahip belirleyin ve gözden geçirme isteyin.
- **Satıcı rakamlarına inanmak.** Yarar iddiaları kontrol edilmez. Bunun yerine kendi vakalarınızda sınayın ve ölçün.
- **Eskimiş dayanak.** Bilgi tabanı yanlıştır ve yapay zeka bunu tekrarlar. Bunun yerine makaleleri güncel ve sahipli tutun.
- **Gizli yanlılık.** Bazı kullanıcılara veya sorunlara daha kötü davranılır. Bunun yerine gruplar arasında test edin ve çıktıları gözden geçirin.
- **Anlamadan otomatikleştirmek.** Yapay zeka kontrol olmadan üretim üzerinde işlem yapar. Bunun yerine öneri ve gözden geçirmeyle başlayın ve eyleme yalnızca güçlü güvencelerle geçin.
- **Kayıt yok.** Kararlar denetlenemez. Bunun yerine neyin sorulduğunun, üretildiğinin ve karara bağlandığının günlüklerini tutun.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Politika ve hesap verebilirlik | Kullanım geçici (ad hoc) ve kayıtsızdır | Bazı ekiplerin kuralları vardır | Yazılı bir politika, kullanım envanteri ve adı belli sahipler vardır | Politika uyumu ve olaylar gözden geçirilir | Politika ekipler, tedarikçiler ve düzenleyiciler arasında hizalanır |
| Kalite ve dayandırma | Çıktıya varsayılan olarak güvenilir | Önemli kullanımlar için bazı kontroller vardır | Yanıtlar onaylı kaynaklara dayandırılır ve gerçek vakalarda test edilir | Hata ve geçersiz kılma oranları ölçülür ve buna göre harekete geçilir | Dayandırma ve testler ekipler arasında paylaşılır ve iyileştirilir |
| Veri koruma ve adalet | Veriler serbestçe yapıştırılır | Bazı veri kuralları vardır | Veri işleme kuralları ve yanlılık kontrolleri rutindir | Veri olayları ve adalet bulguları izlenir ve düzeltilir | Veri ve adalet uygulamaları kurum ve tedarikçiler genelinde eşgüdümlenir |
| Değer ve öğrenme | Değer varsayılır | Bazı denemeler yapılır | Pilotların kararlaştırılmış ölçümleri ve kararları vardır | Yararlar ve maliyetler başlangıç düzeylerine göre ölçülür | Yapay zeka kullanımından öğrenme hizmetler arasında sürekli yayılır |

## Kontrol listesi

- [ ] Hizmetlerimizde veya çevresinde yapay zekanın nerede kullanıldığına dair, resmî olmayan kullanım dahil bir envanterimiz var.
- [ ] Her yapay zeka destekli kullanımdan adı belli bir kişi hesap veriyor.
- [ ] Yazılı bir politika hangi verilerin hangi araçlara girebileceğini söylüyor.
- [ ] Kişisel veriler ve sırlar, onlar için onaylanmamış araçlarla kullanılmadan önce kaldırılıyor veya maskeleniyor.
- [ ] Müşterilere gösterilen veya kararlarda kullanılan yanıtlar onaylı materyale dayanıyor ve gözden geçiriliyor.
- [ ] Gerçek vakalardan oluşan bir test kümemiz var ve değişikliklerden sonra yeniden çalıştırıyoruz.
- [ ] Müşterilere, önemli olduğu yerde otomatik bir sistemin yanıt verdiği söyleniyor ve bir kişiye giden bir yolları var.
- [ ] Geçersiz kılma oranını, hata oranını, kazanılan zamanı ve kullanıcı görüşlerini ölçüyoruz.
- [ ] Yapay zeka destekli önemli kararlar için kayıtlar tutuluyor.
- [ ] Hukuk, güvenlik ve gizlilik personeli kullanımımızı ve aracın koşullarını gözden geçirdi.

## Yapay zeka istemleri

**Amaç: insanların size söylediklerinden bir yapay zeka kullanım envanteri taslağı hazırlamak.**

```text
Help me structure an inventory of AI use in our service organization.

What people have told us they use AI for (paste notes; remove names): [paste].
Tools mentioned: [list].
Types of data involved, as far as we know: [list].

Produce a table with: use, tool, data involved, who is accountable (use "unknown" if not given), risk if wrong (low, medium, high with a one-sentence reason from my notes), and one question to ask. Do not guess about tools or terms I did not mention. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bir yapay zeka asistanı için test kümesi tasarlamak.**

```text
Design a test set for an AI assistant that suggests answers to service desk questions.

The knowledge sources it will use: [describe].
Types of question we get: [list with rough share if you know].
Cases where the right answer is "not in the knowledge base" or "escalate": [describe].

Propose a structure for 100-200 test cases (categories, how to choose real examples, how to record the correct answer and its source), how to score answers (correct, partly correct, wrong, confidently wrong, correctly declined), and how to repeat after changes. Do not invent test content; tell me what to collect. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: bir ekip için tek sayfalık bir yapay zeka kullanım politikası yazmak.**

```text
Draft a one-page AI use policy for [team].

Tools approved: [list, or write "none yet"].
Data we handle (types and sensitivity): [list].
Rules we must follow, with source text from legal, security, or contracts: [paste, or write "none known"].
Roles: [list].

Write plain-language sections: what AI may be used for, what data may and may not be put into tools, what must be checked by a person before use, who is accountable, how to record significant uses, how to report problems. Mark every item that is an assumption. Do not state that any law requires something unless I pasted its text. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: yapay zekanın ürettiği bir yanıtı bir kullanıcıya gitmeden önce gözden geçirmek.**

```text
Here is a draft answer that an AI tool produced for a user question.

The user's question: [paste, with personal data removed].
The knowledge article(s) the answer should be based on: [paste].
The draft answer: [paste].

Check the draft against the article only. List statements that are supported by the article (quote the part), statements that are not supported, anything missing that the user would need, and the tone. Suggest a corrected version that uses only the article. Do not add facts. List what you are unsure of.
```

## Yapay zeka becerileri

- [prompt-engineering](../../../../skills/prompt-engineering/SKILL.md): doğru materyali sağlayan ve belirsizliği soran net istemler yazmak için kullanın.
- [machine-learning-model-card](../../../../skills/machine-learning-model-card/SKILL.md): bir modelin ne için olduğunu, nasıl test edildiğini ve sınırlarını belgelemek için kullanın.
- [data-governance](../../../../skills/data-governance/SKILL.md): hangi verilerin hangi araçlarla kullanılabileceğine karar vermek için kullanın.
- [legal-data-privacy-compliance](../../../../skills/legal-data-privacy-compliance/SKILL.md): yapay zeka kullanımı hakkında hukuk ve gizlilik personeline soruları hazırlamak için kullanın.
- [risk-register](../../../../skills/risk-register/SKILL.md): yapay zekayla ilgili riskleri, sahipleri ve ele alma yöntemlerini kaydetmek için kullanın.

## Temel kaynaklar

- **AIOps** (Wikipedia): BT operasyonları için yapay zekanın, yeteneklerinin ve iddia edilen yararlarının eleştirisiz kısa bir açıklaması.
- **Hallucination (artificial intelligence)** (Wikipedia): yanlış çıktının nedenleri, örnekleri ve azaltma fikirleri.
- **AI Risk Management Framework** (NIST): gönüllü çerçeve ve üretken yapay zeka profili; ayrıntılar için çerçevenin kendisini okuyun.
- **ITIL certifications** (PeopleCert): sahibinin yeni ITIL ve yapay zeka yönetişimi modülü hakkındaki herkese açık ifadeleri.

## Kaynakça

1. AIOps — Wikipedia — https://en.wikipedia.org/wiki/AIOps
2. Hallucination (artificial intelligence) — Wikipedia — https://en.wikipedia.org/wiki/Hallucination_(artificial_intelligence)
3. AI Risk Management Framework — NIST — https://www.nist.gov/itl/ai-risk-management-framework
4. ITIL certifications — PeopleCert — https://www.peoplecert.org/browse-certifications/it-governance-and-service-management/ITIL-1
5. Retrieval-augmented generation — Wikipedia — https://en.wikipedia.org/wiki/Retrieval-augmented_generation
6. Artificial intelligence — Wikipedia — https://en.wikipedia.org/wiki/Artificial_intelligence
7. Large language model — Wikipedia — https://en.wikipedia.org/wiki/Large_language_model
8. Algorithmic bias — Wikipedia — https://en.wikipedia.org/wiki/Algorithmic_bias
9. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
