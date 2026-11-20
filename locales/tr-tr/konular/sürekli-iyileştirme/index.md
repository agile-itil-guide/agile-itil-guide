# Sürekli İyileştirme

**Sürekli iyileştirme, hizmetleri ve çalışma biçimlerini tekrar tekrar biraz daha iyi yapma alışkanlığıdır; iyileştirme işi, her iş gibi görünür, sahipli, takvimli ve denetlenir olduğunda gerçek olur.**

## Bu neden önemli

Bu rehberdeki her uygulama aynı yerde biter: olandan öğrenmek ve bir şeyi değiştirmek. Olaylar sorunlara, sorunlar düzeltmelere, retrospektifler deneylere ve hizmet seviyesi gözden geçirmeleri yeni hedeflere yol açar. Sürekli iyileştirme, bunları birbirine bağlayan ve hareket halinde tutan uygulamadır. Onsuz her uygulama, kimsenin harekete geçmediği içgörüler üretir.

Birçok kuruluşta iyileştirme, ilk sıkıştırılan şeydir. Teslimat baskısı her günü doldurur ve iyileştirme fikirleri kimsenin açmadığı bir belgede birikir. Çevik ekiplerin bir ön avantajı vardır, çünkü retrospektifler yerleşiktir; ancak hiçbir değişiklik üretmeyen retrospektifler yaygındır. Bir sürekli iyileştirme uygulamasının sınaması basittir: bu çeyrekte bu sayede daha iyi olan üç şeyi sayabilir misiniz?

[Sürekli iyileştirme sürecine ilişkin Wikipedia maddesi](https://en.wikipedia.org/wiki/Continual_improvement_process), onu ürünleri, hizmetleri ya da süreçleri iyileştirmeye yönelik, artımlı ya da çığır açıcı, süregelen bir çaba olarak betimler; geri bildirim, verimlilik ve küçük adımlarla evrim temel özellikleridir. [PDCA maddesi](https://en.wikipedia.org/wiki/PDCA), birçok iyileştirme yönteminin arkasındaki planla-uygula-denetle-önlem al döngüsünü betimler. İkisi de geneldir. ITIL sürekli iyileştirmeyi hizmet değer sisteminin bir bileşeni olarak (bkz. Konu 2.3 — ITIL Hizmet Değeri Sistemi) ve bir uygulama olarak ele alır, ancak çerçeve sahibinin metni bu rehber için mevcut değildi; bu nedenle bu konu ITIL'in iyileştirme modelini ayrıntılı olarak betimlemez.

## Temel kavramlar

### Nedir

Wikipedia'ya göre sürekli iyileştirme süreci (CIP), sürekli iyileştirme (continuous improvement) olarak da adlandırılır, ürünleri, hizmetleri ya da süreçleri iyileştirmeye yönelik süregelen bir çabadır. Madde onu kalite, proje ve program yönetimi gibi yönetim sistemleri için bir üst süreç (meta-process) olarak betimler ve üç temel özelliği vardır: geri bildirim, verimlilik ve küçük, artımlı adımlarla evrim. Bir öncü olarak, CIP'yi süreç ve müşteri geri bildirimini kurumsal hedeflere karşı değerlendiren bir sistemin parçası olarak gören W. Edwards Deming'i gösterir.

### Continual ya da continuous

Madde bir terminoloji noktasına dikkat çeker: 1990'ların sonunda ISO 9001:2000'in geliştiricileri "continuous" sözcüğünü "continual" olarak değiştirmiştir; bildirildiğine göre komite adım adım iyileştirmeyi tercih etmiş ve "continuous" sözcüğünün dakika dakika değişikliği ima edebileceğini düşünmüştür. ITIL "continual" kullanır. Pratikte terimler birbirinin yerine kullanılır. Önemli olan, düzenli, yinelenen iyileştirmedir.

### Kaizen

**Kaizen**, kabaca "iyilik için değişiklik" anlamına gelen bir Japonca terimdir. Maddeye göre onu Masaaki Imai'nin 1986 tarihli *Kaizen: The Key to Japan's Competitive Success* kitabı yaygınlaştırmıştır ve özellikleri arasında birçok küçük değişiklik, mevcut çalışanlardan gelen fikirler, düşük maliyet ve çalışan sahipliği yer alır. Bu, işi yapan kişilerin neyin iyileştirileceğini görmek için en iyi konumda olduğu çevik ekiplere uyar (bkz. Konu 1.7 — Yalın Yazılım Geliştirme).

### PDCA döngüsü

PDCA (planla, uygula, denetle, önlem al), Wikipedia'nın ifadesiyle, süreçleri ve ürünleri denetlemek ve sürekli iyileştirmek için yinelemeli bir yöntemdir. Aynı zamanda 1920'lerde Bell Telephone Laboratories'teki Walter Shewhart'ın adından hareketle Shewhart döngüsü olarak da adlandırılır; W. Edwards Deming onu 1940'larda değiştirmiş ve 1950'lerde Japonya'da yönetime uygulamıştır. Adımlar:

| Adım | Ne yaparsınız |
|---|---|
| **Planla (Plan)** | İstediğiniz sonuçları sunmak için gereken hedefleri ve süreçleri belirleyin |
| **Uygula (Do)** | Planı, tercihen küçük ölçekte yürütün |
| **Denetle (Check)** | Topladığınız verileri beklenen sonuçlarla karşılaştırın ve eğilimlere bakın |
| **Önlem al (Act)** | Sorunların kök nedenlerini araştırın, süreci ayarlayın ve bir sonraki döngüyü başlatın |

Madde PDCA'yı bilimsel yönteme ve onun hipotez, deney, değerlendirme örüntüsüne bağlar. Bir değişken olan PDSA, "denetle" yerine Deming'in tercih ettiği "çalış (study)" sözcüğünü koyar. Madde yinelemenin merkezi olduğunu söyler: her döngü bilgiyi rafine eder. Bir değişikliğe belirtilmiş bir beklenti ve bir denetimle "deney" diyen ekipler bu örüntüyü kullanmaktadır.

### İyileştirme nereden gelir

Bir hizmet kuruluşunda iyileştirme fikirleri birçok yerden gelir:

| Kaynak | Örnek | Nerede ele alındığı |
|---|---|---|
| Olaylar ve olay sonrası incelemeler | Bir arıza eksik bir uyarıyı gösterir | Konu 3.2 — Olay Yönetimi |
| Sorun araştırması | Yinelenen kesintiler bir tasarım kusurunu gösterir | Konu 3.3 — Sorun Yönetimi |
| Hizmet masası temaları | Aynı soru her hafta gelir | Konu 3.1 — Hizmet Masası |
| Retrospektifler | Ekip devir işlemlerini yavaş bulur | Konu 1.4 — Teslimat Tahmini ve Planlama Metrikleri |
| Akış verileri | Bir kuyruk bir adımda büyür | Konu 1.5 — Kanban |
| Müşteri geri bildirimi | Kullanıcılar bir formu kafa karıştırıcı bulur | Konu 3.6 — Hizmet Talebi Yönetimi |
| Hizmet seviyesi gözden geçirmeleri | Bir hedef tekrar tekrar kaçırılır | Konu 3.7 — Hizmet Seviyesi Yönetimi |
| Denetimler ve risk gözden geçirmeleri | Bir denetimin zayıf olduğu bulunur | Konu 5.7 — Yönetişim, Risk ve Uyum |

Sürekli iyileştirme uygulaması bunları tek bir görünür listede toplar, ne yapılacağını seçer ve sonuçları denetler.

### Bir iş olarak iyileştirme

Merkezi disiplin, iyileştirmeyi iş olarak ele almaktır: sahipleri, beklenen faydaları ve tarihleri olan bir biriktirme listesindeki kalemler. Onsuz iyileştirme coşkuya ve boş zamana bağlıdır. Bu aynı zamanda teslimat işiyle ödünleşimi açıkça yapmak anlamına gelir; böylece kapasite bilinçli olarak korunur. Yaygın bir düzenleme, her döngünün bir payını iyileştirmeye ayırmak ya da teslimatın yanında kısa iyileştirme döngüleri yürütmektir.

### İyileştirmeyi ölçmek

Bir şeyin iyileştiğini bilmek için öncesi ve sonrası gerekir. Hizmeti geri getirme süresi, yinelenen olaylar ya da bekleme süresi gibi değişiklikle ilgili bir ölçü seçin ve öncesine ve sonrasına bakın. Hiçbir şeyi iyileştirmeden kolayca oynatılabilen ölçülerden kaçının. Birkaçını kullanın ve sayıların ne anlama geldiğini tartışın (bkz. Konu 5.6 — Metrikler ve Ölçüm). Başvurulan maddeler iyileştirme programlarının etkililiğine dair kanıt vermez; bu nedenle ekiplerin kendi sonuçları kanıttır.

### Yöntemler

Birçok yöntem iyileştirmeyi destekler: kök neden çözümlemesi, kusurların veriye dayalı azaltılması için Six Sigma ve DMAIC, değer akışı haritalama ve kaizen etkinlikleri. Sürekli iyileştirmeye ilişkin Wikipedia maddesi Six Sigma'dan, DMAIC'ten ya da ITIL iyileştirme modelinden söz etmez, bu yüzden bu rehber bunları ona atfetmez. Yöntemleri sorunun büyüklüğüne uydurun: küçük bir sürtünme için bir retrospektif eylemi, kalıcı bir kusur için veriye dayalı bir proje.

### Sınırlar

Madde sürekli iyileştirmeye yönelik hiçbir eleştiri kaydetmez ve kaynaklarından bazıları zayıf ya da eskidir. Pratik riskler iyi bilinir: çok fazla değişiklik geldiğinde iyileştirme yorgunluğu, listelerin büyüdüğü ve hiçbir şeyin değişmediği iyileştirme tiyatrosu ve bir ekibin kendi parçasını iyileştirip bütünü kötüleştirdiği yerel eniyileme. Bunlara karşı kısa, görünür bir liste ve sonuçların düzenli denetimiyle önlem alın.

## İyi uygulamalar

1. **Tek bir görünür iyileştirme listesi tutun.** Olaylardan, retrospektiflerden, geri bildirimlerden ve gözden geçirmelerden gelen fikirleri tek bir yerde toplayın. Her kaleme bir sahip, ele aldığı sorunu ve beklenen faydayı verin.
2. **İyileştirme kalemlerini iş olarak ele alın.** Bunları teslimat kalemlerinin yanında biriktirme listesine koyun ve planlamada ne kadar kapasite alacaklarına karar verin. Baskı arttığında bu payı koruyun.
3. **Az seçin ve bitirin.** Aynı anda en değerli bir ila üç kalem üzerinde çalışın. Başlanmış kalemlerin uzun bir listesi, iyileştirme tiyatrosunun işaretidir.
4. **Döngüyü kullanın.** Her değişiklik için planı ve beklenen sonucu belirtin, değişikliği küçük ölçekte yapın, verileri denetleyin ve benimseme, ayarlama ya da bırakma konusunda karar verin. Kararı yazın.
5. **Başlamadan önce başarıyı tanımlayın.** Değişiklikten önce ölçüyü ve görmeyi beklediğinizi seçin. Bu, sonradan her sonucun bir başarı olarak açıklanmasını önler.
6. **Küçük ve yerel başlayın.** Ekiplerin net sınırlar içinde izin beklemeden kendi işlerini iyileştirmesine izin verin. Daha büyük programları ekipler arasını kesen sorunlara saklayın.
7. **Öğrendiklerinizi paylaşın.** Neyin değiştiğine ve ne olduğuna dair, başarısızlıklar dahil, kısa notlar yayımlayın. Diğer ekipler bunu yeniden kullanabilir ya da kaçınabilir.
8. **Tüm sisteme bakın.** Bir iyileştirmeyi benimsemeden önce kimi etkilediğini sorun. Başka bir ekibe iş ekleyen yerel bir kazanç, bütünde bir iyileştirme değildir (bütüncül düşünme için bkz. Konu 2.4 — ITIL Yol Gösterici İlkeleri).
9. **Listeyi düzenli olarak gözden geçirin.** Ayda bir, listeye ekip ve hizmet sahibiyle birlikte bakın: nelerin bittiği, nelerin takıldığı, nelerin bırakılması gerektiği. Anlamını yitirmiş kalemleri kaldırın.
10. **Etkinliği değil, sonuçları kutlayın.** Kullanıcılar ya da personel için işleri kanıtla iyileştiren iyileştirmeleri takdir edin. Fikir ya da toplantı sayısını ödüllendirmeyin.
11. **Yöntemi soruna uydurun.** Küçük sorunlar için hızlı deneyler, kalıcı kusurlar için veriye dayalı yöntemler kullanın ve karmaşık olanlar için uzman yardımı getirin.
12. **Kullanıcıları ve tedarikçileri dahil edin.** Onlara neyin iyileştirileceğini sorun ve etkilendikleri yerlerde sonuçları gözden geçirmeye davet edin (bkz. Konu 3.14 — Tedarikçi Yönetimi).

## Ekibinizle tartışılacak sorular

**Değiştirmeye karar verdiğimiz bir şey sayesinde son çeyrekte ne daha iyi oldu?**

Kanıtlı belirli örnekler isteyin. İnsanlar zorlanıyorsa bulgu budur. Örnekler varsa, onları neyin işlettiğini sorun: bir sahip, zaman, net bir ölçü. Takılan iyileştirmelerle karşılaştırın. Kolaylaştırıcı hangi örüntünün ekibinizde daha yaygın olduğunu sorabilir.

**İyileştirme fikirlerimiz nereye gidiyor?**

Birkaç yakın tarihli fikri izleyin: bir olay gözden geçirmesinden, bir retrospektiften, bir müşteri yorumundan. Her birinin nerede sonlandığını bulun. Çoğu zaman belgelere ve biletlere dağılmışlardır. Tek bir listeyi, onu kimin sürdürdüğünü ve nasıl gözden geçirildiğini tartışın. İlk sürümünü oturumda oluşturun.

**Kapasitemizin ne kadarı iyileştirmeye gidiyor ve buna kim karar verdi?**

Son birkaç döngüye bakın ve payı tahmin edin. Çoğu zaman insanların inandığından çok daha küçüktür ve kimse bunu seçmemiştir. Ekibin ve yöneticilerin ne olması gerektiğini düşündüğünü sorun. Başlangıç payı ve onu korumanın bir yolu üzerinde uzlaşın.

**Değişikliklerimizden hangilerini sonradan denetledik?**

Son üç değişikliği ve işe yaradıklarını hangi kanıtın gösterdiğini sorun. Birçoğu hiç denetlenmemiştir. Basit bir alışkanlığı tartışın: değişiklikten önce ne görmeyi beklediğinizi ve ne zaman bakacağınızı belirtin. Bunu uygulamak için mevcut bir değişiklik seçin.

**Hangi iyileştirme bize yardımcı oldu ve başkasına zarar verdi?**

Bir sorunu başka yere taşıyan yerel iyileştirmelerden örnekler toplayın. Bunlar çoğunlukla devir işlemlerindeki ya da onaylardaki değişikliklerden gelir. Etkilenen kişilere daha erken nasıl sorulacağını tartışın. Amaç, bir değişiklikten önce sorulacak basit bir sorudur.

**İyileştirme listemizdeki en eski kalem nedir ve neden hâlâ orada?**

En eski kalemi seçin ve geçmişini izleyin. Nedenler arasında sahip olmaması, zaman olmaması, anlaşmazlık ya da olayların onu geçmesi yer alır. Yapmaya, takvime koymaya ya da açıkça bırakmaya karar verin. Bir kalemi bilerek bırakmak, sağlıklı bir listenin işaretidir.

## Uygulamada: çevik bir ITIL örneği

Bölgesel bir su idaresinin, on bir kişilik bir ekip tarafından işletilen bir müşteri faturalandırma ve sayaç okuma platformu var. Retrospektifler iki haftada bir yapılıyor ve eylem listeleri üretiyor, ancak azı tamamlanıyor. Olaylar gözden geçiriliyor ve bu gözden geçirmelerden çıkan eylemler ayrı bir sisteme kaydediliyor. İdarenin düzenleyicisi, idarenin hizmet arızalarından nasıl öğrendiğine dair kanıt istedi.

Hizmet sahibi ve ekip lideri iyileştirmeyi görünür kılmaya karar veriyor. Retrospektiflerden, olay gözden geçirmelerinden ve müşteri geri bildirimlerinden gelen eylemleri toplayan tek bir iyileştirme listesi oluşturuyorlar. Her kalemin bir sahibi, bir sorun ifadesi, beklenen fayda ve bir ölçüsü var. Her iki haftalık döngünün yüzde 15'ini iyileştirme kalemlerine ayırıyorlar ve devam edenlerin sayısını üçle sınırlıyorlar. Her biri için planla, uygula, denetle ve önlem al adımlarını izliyorlar: ne görmeyi beklediklerini yazıyorlar, değişikliği bir alt kümede deniyorlar, belirli bir süreden sonra sayılara bakıyorlar ve kararı kaydediyorlar. Hizmet sahibi ve bir müşteri hizmetleri temsilcisiyle aylık bir gözden geçirme, nelerin yapıldığına ve nelerin öğrenildiğine bakıyor.

Altı ay sonra ekip dokuz kalemi tamamlamış durumda; bunlar arasında yinelenen bir sayaç verisi içe aktarma arızası için, o neden kaynaklı yinelenen olayları sıfıra yakın düşüren bir düzeltme ve konuyla ilgili çağrıları azaltan daha net bir fatura açıklaması var. Düzenleyici için liste ve denetimler biçiminde kanıtı da var. Bazı zorluklar sürüyor. İki kalem döngü ilerlediği için denetlenmeden tamamlandı ve içe aktarma sürecindeki bir iyileştirme, ancak bir ay sonra ortaya çıkan, aşağı akıştaki bir raporlama ekibinin işini yavaşlattı. Ekip liste şablonuna bir "başka kim etkileniyor" sorusu ve her denetim için bir takvim hatırlatıcısı ekliyor.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri iyileştirme listesinin büyük bölümüne sahiptir. Retrospektiflerden ve olaylardan gelen fikirleri tek bir yere getirin, başladığınızı bitirin ve sonuçları denetleyin. Kapasiteyi yalnızca yeni özelliklere değil, iyileştirmeye de harcamaya istekli olun.

### Hizmet ve operasyon ekipleri

Operasyon ekipleri sürtünmeyi ilk görenlerdir. Olay temalarını, masa iletişimlerini ve akış verilerini listeye besleyin ve sonuçları denetlemeye katılın. Angaryayı ve yinelenen olayları azaltan iyileştirmeler için gerekçe sunun.

### Liderlik ve yönetişim

Liderler iyileştirme kapasitesini korur ve sonuçları sorar. Kaç fikir olduğunu değil, neyin iyileştiğini ve nasıl denetlendiğini sorun. Ekiplerin adlandırdığı engelleri kaldırın ve bunu yaptığınızı gösterin. Ekip sınırlarını aşan iyileştirmeleri destekleyin.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar en iyi fikirlerin bir kısmını sağlar. Sizi neyin hayal kırıklığına uğrattığını ekibe söyleyin ve sonuç olarak neyin değiştiğini duymayı isteyin. Hizmetinizi ilgilendiren gözden geçirmelere katılın. Bir değişikliğin yardımcı olup olmadığına dair geri bildiriminiz, var olan en doğrudan denetimdir.

## Yaygın başarısızlık biçimleri

- **Sahipsiz fikirler.** Liste büyür ve hiçbir şey yapılmaz. Bunun yerine her kalem için bir sahip ve beklenen fayda isteyin.
- **Boş zaman olarak iyileştirme.** Teslimat onu dışarı iter. Bunun yerine kapasite ayırın ve koruyun.
- **Aynı anda çok fazla.** Her şey başlanır ve azı biter. Bunun yerine iyileştirme kalemleri için devam eden işi sınırlayın.
- **Denetim yok.** Değişiklikler planlandıkları için benimsenir. Bunun yerine beklenen sonucu önceden belirtin ve verilere bakın.
- **Yerel eniyileme.** Bir ekip iyileşir, başkası zarar görür. Bunun yerine öncesinde ve sonrasında kimin etkilendiğini sorun.
- **İyileştirme tiyatrosu.** Çalıştaylar ve afişler sonuçların yerini alır. Bunun yerine tamamlanmış ve doğrulanmış iyileştirmeleri sayın.
- **Oyunlaştırılabilen ölçüler.** Sayı kıpırdar ve hiçbir şey iyileşmez. Bunun yerine birkaç ölçü kullanın ve altta yatan işe bakın.
- **Paylaşmayı unutmak.** Dersler ekipte kalır. Bunun yerine kısa notlar yayımlayın ve başkalarını yeniden kullanmaya davet edin.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Toplama ve önceliklendirme | Fikirler dağınık ve önceliksizdir | Bazı ekipler liste tutar | Ekip başına sahipler ve beklenen faydalarla tek bir görünür liste | Öncelikler etki ve emek verilerini kullanır | İyileştirme listeleri ekipler arasında ve müşterilerle hizalanır |
| Kapasite ve akış | İyileştirme boş zamanda yapılır | Bir miktar kapasite ayrılır | Korunan bir kapasite payı ve devam eden iş sınırları | İyileştirmenin kapasitesi ve işlem hacmi gözden geçirilir | Kapasite, ekipleri kesen iyileştirmeler için ekipler arasında paylaşılır |
| Sonuçları denetleme | Sonuçlar denetlenmez | Bazı değişiklikler gözden geçirilir | Her değişikliğin belirtilmiş bir beklentisi ve bir denetimi vardır | Sonuçlar ölçülür ve kararlara bağlanır | Kanıt ekipler arasında paylaşılır ve kuruluşa yol göstermek için kullanılır |
| Öğrenme ve yayılma | Dersler yerel kalır | Bazı notlar paylaşılır | Dersler yayımlanır ve gözden geçirilir | İyileştirmelerin yeniden kullanımı izlenir | İyileştirmeler ekipler ve tedarikçiler arasında rutin olarak yayılır |

## Kontrol listesi

- [ ] Sahipleri ve beklenen faydaları olan tek bir görünür iyileştirme listemiz var.
- [ ] Retrospektiflerden, olay gözden geçirmelerinden, masa temalarından ve geri bildirimlerden gelen fikirlerin hepsi listeyi besliyor.
- [ ] Her döngünün korunan bir payı iyileştirme kalemlerine gidiyor.
- [ ] Devam eden iyileştirme kalemlerinin sayısını sınırlıyoruz.
- [ ] Her değişiklik beklenen bir sonuç ve onu denetlemek için bir zaman belirtiyor.
- [ ] Sonuçları denetliyor ve benimseme, ayarlama ya da bırakma kararını kaydediyoruz.
- [ ] Bir değişiklik yapmadan önce başka kimin etkilendiğini soruyoruz.
- [ ] Liste en az ayda bir gözden geçiriliyor.
- [ ] Neyin değiştiğine ve ne öğrendiğimize dair kısa notlar paylaşıyoruz.
- [ ] Bu çeyrekte iyileştirme çalışması sayesinde daha iyi olan üç şeyi sayabiliyoruz.

## Yapay zeka istemleri

**Amaç: iyileştirme fikirlerini tek bir önceliklendirilmiş listede birleştirmek.**

```text
Here are improvement ideas from several sources over the last [period]: [paste items from retrospectives, incident reviews, desk themes, and feedback, one per line, with their source].

Merge duplicates, group related items, and produce a list with: a one-line problem statement for each, the source, what benefit it might bring (use only what the text implies, otherwise write "unknown"), and a question about effort. Do not rank by guesswork; instead propose a way to rank (for example by repeat count and user impact) and apply it only to data I gave. List what you are unsure of.
```

**Amaç: bir iyileştirme fikrini küçük bir deneye dönüştürmek.**

```text
Help me turn this improvement idea into a small experiment using plan, do, check, act.

The idea: [describe].
The problem it addresses, with evidence: [paste facts].
Who is affected: [list teams and users].
Measures we already have: [list].

Write: a hypothesis in one sentence, the smallest change that could test it, how long to run it, what we will measure before and after (leave targets as [to be agreed]), who else to ask before we start, and what decision rule we will use at the end. Do not invent baseline data. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Amaç: bir iyileştirme listesinin durumunu gözden geçirmek.**

```text
Here is our improvement list with status, owner, age, and expected benefit: [paste].

Using only this text, identify: items with no owner; items older than [period] with no progress; items whose expected benefit is unclear; and items that look related and could be combined. For each, suggest a question to ask at the monthly review. Do not decide for us what to drop. List what you are unsure of.
```

**Amaç: bir iyileştirmenin işe yarayıp yaramadığını denetlemek.**

```text
We made this change: [describe] on [date].

Measure before the change, with dates and values: [paste real data].
Measure after, with dates and values: [paste real data].
What else changed in the same period: [list, or write "unknown"].

Describe in plain words what the data shows, without claiming the change caused it if other changes could explain it. Suggest additional checks, and say whether the data is enough to decide to adopt, adjust, or drop. Do not invent numbers or statistics. List what you are unsure of.
```

## Yapay zeka becerileri

- [kaizen](../../../../skills/kaizen/SKILL.md): küçük, sürekli iyileştirmeleri planlamak ve gözden geçirmek için kullanın.
- [agile-reflection](../../../../skills/agile-reflection/SKILL.md): sahipli eylemler üreten retrospektifler yürütmek için kullanın.
- [dmaic](../../../../skills/dmaic/SKILL.md): kalıcı kusurların, tanımla, ölç, çözümle, iyileştir ve denetle aşamalarıyla veriye dayalı iyileştirilmesi için kullanın.
- [six-sigma](../../../../skills/six-sigma/SKILL.md): değişkenlik ve kusurlar ana sorun olduğunda ve istatistiksel bir yaklaşıma ihtiyaç duyduğunuzda kullanın.
- [futurespective](../../../../skills/futurespective/SKILL.md): birlikte ileriye bakmak ve bir sonraki dönem için iyileştirmeler üzerinde uzlaşmak için kullanın.

## Temel kaynaklar

- **Continual improvement process** (Wikipedia): tanım, kaizen, PDCA ve continual ile continuous terminolojisi.
- **PDCA** (Wikipedia): planla-uygula-denetle-önlem al döngüsü, kökenleri ve PDSA gibi değişkenleri.
- **Kaizen** (Wikipedia): küçük, sürekli iyileştirme ve Japon sanayisindeki kökenleri üzerine arka plan.
- **Lean software development** (Wikipedia): yazılım işinde sürekli iyileştirmenin arkasındaki yalın fikirler.

## Kaynakça

1. Continual improvement process — Wikipedia — https://en.wikipedia.org/wiki/Continual_improvement_process
2. PDCA — Wikipedia — https://en.wikipedia.org/wiki/PDCA
3. Kaizen — Wikipedia — https://en.wikipedia.org/wiki/Kaizen
4. W. Edwards Deming — Wikipedia — https://en.wikipedia.org/wiki/W._Edwards_Deming
5. Walter A. Shewhart — Wikipedia — https://en.wikipedia.org/wiki/Walter_A._Shewhart
6. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
7. Six Sigma — Wikipedia — https://en.wikipedia.org/wiki/Six_Sigma
8. Root cause analysis — Wikipedia — https://en.wikipedia.org/wiki/Root_cause_analysis
9. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
