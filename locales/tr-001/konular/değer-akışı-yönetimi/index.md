# Değer Akışı Yönetimi

**Değer akışı yönetimi, talepten değere uzanan yolun tamamına bakar, işin nerede beklediğini ölçer ve ekipler arası akışı iyileştirir; çünkü bir hizmet kuruluşundaki en büyük gecikmeler genellikle ekiplerin içinde değil, arasındadır.**

## Bu neden önemli

Çoğu ekip kendi işini ölçer: kapatılan kayıtlar, bitirilen hikâyeler, yayımlanan değişiklikler. Müşteri haftalarca beklerken bu sayılar iyi görünebilir. Nedeni, tipik bir talepte geçen sürenin çoğunun beklemekle, kuyruklarda, onaylarda, ekipler arasında geçmesidir. Kendi adımını hızlandıran bir ekip, talepte bulunan kişi için hiçbir şeyi değiştirmeyebilir.

Yalın düşüncenin bunu görmek için bir yöntemi vardır: bir sürecin başından müşteriye kadar her adımı çizen ve her aşamada süreyi ve hacmi kaydeden değer akışı haritası. ITIL 4'ün de değer akışı için kendi fikri vardır: bir hizmeti yaratan ve sunan, değer zinciri etkinliklerini farklı sıralarda birleştiren bir etkinlikler kümesi (bkz. Konu 2.6 — Hizmet Değer Zinciri). İkisi birbirine uyar. ITIL fikri bir akışın ne olduğunu söyler, yalın yöntem de birini nasıl ölçüp iyileştireceğinizi gösterir.

Değer akışı yönetimi tek seferlik bir haritalama atölyesinin ötesine geçer. İşin akışını sürekli yönetmek anlamına gelir: ortak ölçümler, adı belli bir sahip ve akıştaki her ekibi içeren düzenli gözden geçirmelerle. DORA'nın yetkinlik listesi değer akışındaki işin görünürlüğünü ve devam eden iş sınırlarını içerir ve sınırlara dair rehberliği, ekibin dışındaki iş dahil tüm işi görünür kılmayı anlatır. Bu konu Wikipedia'daki değer akışı haritalama maddesinden, DORA'dan ve Kanban Kılavuzu'ndan yararlanır ve kaynakların sustuğu yerleri belirtir.

## Temel kavramlar

### Değer akışı nedir

**Değer akışı**, bir talebin teslim edilmiş değere dönüştüğü adımlar dizisidir. [Wikipedia'daki değer akışı haritalama maddesi](https://en.wikipedia.org/wiki/Value-stream_mapping) yöntemi, bir ürünü veya hizmeti bir sürecin başından müşteriye taşıyan etkinlikler için mevcut durumu çözümleyen ve bir gelecek durum tasarlayan yalın yönetim tekniği olarak anlatır. ITIL görüşünde bir değer akışı, müşterilere belirli bir hizmeti veya ürünü yaratan ve sunan belirli bir etkinlikler kümesidir (bkz. Konu 2.6 — Hizmet Değer Zinciri).

Bir hizmet kuruluşundaki örnekler: bir olayı bildirimden onarıma ele almak, bir değişikliği fikirden üretime teslim etmek, yeni bir müşteriyi devreye almak veya bir erişim talebini yerine getirmek.

### Değer akışı haritalama

Madde, ortaya çıkan görsel haritanın her kritik adımı gösterdiğini ve her aşamadaki süreyi ve hacmi nicelleştirdiğini söyler. İki harita anlatır: malzeme ve bilginin gerçek akışının gözlemlenip izlenmesiyle oluşturulan **mevcut durum haritası** ve iyileştirmelerden sonraki ideal süreci gösteren **gelecek durum haritası**. Önce mevcut durum oluşturulmalıdır. Madde, Mike Rother ve John Shook'un *Learning to See* (Lean Enterprise Institute, 1999) kitabını kaynak olarak anar. Kullanım alanları olarak yazılım geliştirmeyi, ürün geliştirmeyi, proje yönetimini ve idari ve ofis süreçlerini listeler ve Ali ve arkadaşlarının iki yazılım odaklı yaklaşımını anar: geliştirme yapıtlarının analizi ve bilgi akışının analizi.

Madde teslim süresini (lead time), süreç süresini veya tamam ve doğru yüzdesini tanımlamaz, simgeleri listelemez ve eleştiri tartışmaz. Ancak DORA'nın sürekli teslimat sayfası, değer akışı haritalamayı geçen süreyi değer katan süreyle karşılaştırarak ve tamam ve doğru yüzdesini (%C/A) ölçerek darboğazları açığa çıkarmanın bir yolu olarak anar. Aşağıdaki terimler yaygın kullanımdır:

| Terim | Yaygın kullanımdaki anlamı |
|---|---|
| **Teslim süresi (lead time)** | Bir talebin başlangıcından teslimine kadar geçen toplam süre |
| **Süreç süresi** (veya dokunma süresi) | Birinin talep üzerinde gerçekten çalıştığı süre |
| **Bekleme süresi** | Talebin adımlar arasında boşta durduğu süre |
| **Tamam ve doğru yüzdesi (%C/A)** | Bir adıma gelen işin düzeltme veya eksik bilgi gerektirmeyen payı |
| **Akış verimliliği** | Süreç süresinin teslim süresine bölünmesi, yüzde olarak |

Akış verimliliği, bu kılavuzun örneklemesi için hesaplanan basit bir orandır ve okunan kaynaklar onu tanımlamaz.

### Akış ölçümleri

Kanban Kılavuzu dört akış ölçümü adlandırır (bkz. Konu 1.5 — Kanban): **devam eden iş** (başlanmış ama bitmemiş öğeler), **çıktı hızı** (dönem başına bitirilen öğeler), **iş öğesi yaşı** (bitmemiş bir öğenin başlamasından bu yana geçen süre) ve **çevrim süresi** (tamamlanmış bir öğe için başlangıçtan bitişe süre). Bunlar bir ekibin iş akışı düzeyinde çalışır. Değer akışı yönetimi aynı fikirleri ekipler arasında uygular: geçen süreyi, tek bir ekibin onu aldığı noktadan değil, talepten müşterinin teslim almasına kadar ölçün.

DORA'nın değişiklik teslim süresi gibi yazılım teslimat ölçümleri akışın bir dilimine, işleme almadan üretime kadar olan kısma uygulanır (bkz. Konu 3.4 — Değişiklik Sağlama). Daha önceki kısım, fikirden işlemeye, de değer akışının parçasıdır ve çoğu zaman en uzun beklemeleri barındırır.

### Devam eden iş sınırları

DORA'nın devam eden iş (WIP) sınırları sayfası bunları, bir iş akışının her aşamasında kaç öğenin bulunabileceğine konan üst sınırlar olarak anlatır. DORA araştırmasının WIP sınırlarını daha iyi yazılım teslimat performansıyla yalnızca görsel panolar ve izlemeden gelen geri bildirim döngüleri gibi diğer yetkinliklerle birlikte ilişkilendirdiğini söyler ve etki büyüklüğü vermez. Uygulama tavsiyeleri arasında ekibin dışındaki iş dahil tüm işi görünür kılmak, her sınırı ekip kapasitesine göre belirlemek, sınırları sıkı tutmak ve insanlar boştayken yükseltmemek, işi yalnızca bir yuva açıldığında çekmek, teslim süresini ve değişkenliğini izlemek, devirleri azaltmak ve sonraki kısıtı açığa çıkarmak için sınırları kademeli olarak düşürmek vardır. Adlandırdığı tuzaklar arasında yerel optimizasyona yol açan yukarı ve aşağı akış işini yok saymak ve sınırları çok yüksek belirlemek yer alır.

### Akışın tamamını görmek

"Yerel optimizasyon" tuzağı merkezi olandır. Beş ekipli bir akışın beş kuyruğu vardır. Bir ekip hızını ikiye katlarsa akışın teslim süresi neredeyse hiç değişmeyebilir; çünkü diğerleri hâlâ beklemektedir. Değer akışı yönetimi, bütünü sınırlayan adım olan **kısıtı** arar ve önce onu iyileştirir (bütünün optimizasyonu için bkz. Konu 1.7 — Yalın Yazılım Geliştirme).

### Sahiplik ve yönetişim

Bir akış ekipleri keser, bu yüzden bütünden sorumlu birine ihtiyaç duyar. Bir değer akışı sahibi (veya küçük bir grup) haritayı, ölçümleri ve iyileştirme listesini tutar ve ekipleri toplar. Sahip olmadan kimse akıştan sorumlu olmaz ve iyileştirmeler ekip sınırları içinde kalır. Bu, ürün ve hizmet sahipliğine bağlanır (bkz. Konu 5.5 — Ürün ve Hizmet Sahipliği).

### Araçlar

Değer akışı yönetimi için yazılım araçları, araç zinciri genelindeki akışı göstermek için kayıt sistemlerinden, kaynak denetiminden ve hatlardan veri toplar. Bu kılavuz için okunan kaynaklar bu tür araçları ele almaz. Herhangi birini değerlendirirseniz hangi veriye ihtiyaç duyduğunu, ne kadar doğru olduğunu ve ölçümlerin sizin bir sorunuzu yanıtlayıp yanıtlamadığını kontrol edin. İlgili ekiplerle elle çizilmiş kaba bir harita, başlamak için iyi bir yerdir ve çoğu zaman bir panodan daha fazlasını gösterir.

### Sınırlar

Wikipedia maddesi hiçbir eleştiri tartışmaz ve DORA WIP sayfası etki büyüklüğü veya hedef değer vermez. Deneyim olarak sunulan pratik uyarılar arasında hiçbir değişikliğe yol açmayan haritalama, ekipleri sıralamak için kullanılan ölçümler ve gerçek öğelerin gözlemi yerine yöneticilerin hafızasından çizilen haritalar vardır.

## İyi uygulamalar

1. **Önemli olan tek bir akış seçin.** Kullanıcıların önemsediği bir akış seçin; üretime ulaşan bir değişiklik veya bir erişim talebi gibi. Dar, gerçek bir akış, geniş, soyut bir akıştan daha çok şey öğretir.
2. **Gerçek öğelerden haritalayın.** Birkaç yakın tarihli öğeyi baştan sona izleyin ve süreç belgesini değil, gerçek tarihleri kaydedin. Gözlem, maddenin gerçek akışı gözlemlemeye ve izlemeye yaptığı vurgunun düşündürdüğü gibi, hatırlamayı yener.
3. **Her adımda süreyi ve beklemeyi kaydedin.** Her adım için çalışma süresini ve öncesindeki beklemeyi not edin. Hikâye genellikle beklemelerdedir.
4. **Akıştaki herkesi dahil edin.** Öğeye dokunan her ekipten, onaylayanlar ve tedarikçiler dahil, insanları davet edin. Haritalamayı birlikte yapın; böylece kimse sonuca şaşırmaz.
5. **Teslim süresini, süreç süresini ve akış verimliliğini hesaplayın.** Geçen süreyi çalışma süresiyle karşılaştırın ve ne kadarının beklemek olduğuna bakın. Sayıları konuşmaları başlatmak için kullanın.
6. **Doğruluğa bakın.** İşin bir adıma ne sıklıkla eksik veya yanlış gelip yeniden iş gerektirdiğini sorun. Tamam ve doğru yüzdesi düşük bir adım aşağı akışta gecikmeye yol açar.
7. **Kısıtı bulun.** Tüm akışı sınırlayan adımı belirleyin ve önce onu iyileştirin. Diğer adımları iyileştirmek az yarar sağlar.
8. **Gelecek durumu çizin.** Ekiplerle ideal olanı değil, daha iyi bir akış tasarlayın ve ilk bir veya iki değişikliği seçin. Sahiplerde ve tarihlerde anlaşın.
9. **Devam eden işi sınırlayın.** Her aşamanın tuttuğuna üst sınır koyun, sınırları kapasiteye göre belirleyin, insanlar boştayken koruyun ve DORA'nın rehberliğinin anlattığı gibi kademeli olarak düşürün.
10. **İşi görünür kılın.** Akışı, tek bir ekibin dışındaki işi de içeren paylaşılan bir panoda veya haritada gösterin. Öğeler hareket ettikçe güncelleyin.
11. **Bir akış sahibi belirleyin.** Akışın performansından sorumlu, ekipleri toplayabilen ve iyileştirmeleri liderlere taşıyabilen bir kişi seçin.
12. **Düzenli gözden geçirin.** Teslim süresinin, beklemelerin ve iyileştirme listesinin kısa, aylık bir gözden geçirmesini yapın. Önemli değişikliklerden sonra haritayı yeniden çizin.

## Ekibinizle tartışılacak sorular

**Bir talebi ilk temastan müşterinin teslim almasına kadar izlesek ne kadar sürerdi ve bunun ne kadarı çalışma süresi?**

Yakın tarihli bir öğe seçin ve tarihleri toplayın. İnsanlardan bakmadan önce yanıtı tahmin etmelerini isteyin. Tahmin genellikle iyimserdir. Çalışma süresinin payını hesaplayın. Kolaylaştırıcı en büyük beklemenin nerede olduğunu ve sahibinin kim olduğunu sorabilir. İlk hedef olarak onu seçin.

**Akıştaki kimlerle hiç konuşmadık?**

Bir öğenin dokunduğu ekipleri, onaylayanları ve tedarikçileri listeleyin. Ekibin hiç tanışmadıklarını işaretleyin. Onları bir haritalama oturumuna davet etmekle ne kazanılacağını sorun. Tipik yanıtlar: neden beklediklerini anlamak veya daha hızlı çalışmak için neye ihtiyaç duyduklarını anlamak. Birini davet edin.

**Neyi eksik devrediyoruz ve neyi eksik teslim alıyoruz?**

Yeniden iş için geri dönen işin örneklerini isteyin. Hangi devirlerin en çok geri dönüşe yol açtığını ve neyin eksik olduğunu not edin. Bu, tamam ve doğru yüzdesi fikrinin sade anlatımıdır. Bir devir için kısa bir kontrol listesinde anlaşın.

**Akışımızda kısıt nerede ve başka bir şeyi hızlandırırsak ne olur?**

En uzun kuyruğun hangi adımda olduğunu tartışın. Başka bir adımın hızı ikiye katlanırsa uçtan uca sürenin ne olacağını sorun. Amaç, kısıt olmayanı iyileştirmenin çok az şey değiştirdiğini görmektir. Kısıt üzerinde çalışmayı seçin.

**Her ekip aynı anda kaç şey üzerinde çalışıyor ve bir sınır koysak ne olurdu?**

Ekip başına devam eden işi sayın. Yeni iş başlatmayı bırakmanın ne anlama geleceğini tartışın. Tipik korkular: önemli bir şey bekleyecek. Tipik yararlar: işler bitiyor. Bir ekip için deneme sınırında ve sonucu yargılamanın bir yolunda anlaşın.

**Bu akıştan bir bütün olarak kim sorumlu?**

Ekipten kişiyi adlandırmasını isteyin. Kimse yoksa kimin olabileceğini ve hangi yetkiye ihtiyaç duyacağını tartışın. Kolaylaştırıcı, ekipler arası iyileştirmelerin sahip olmadan nadiren gerçekleştiğini not edebilir. Bir isim önerin ve ilgili liderin önüne götürün.

## Uygulamada: çevik bir ITIL örneği

Ulusal bir çevre düzenleyici kurum sanayi işletmecilerine izin verir. Başvuranlar tipik bir iznin yaklaşık dört ay sürdüğünden şikâyet ediyor ve kurumun on iki kişilik dijital hizmetler grubundan bunu hızlandırması isteniyor. Grup zaten daha hızlı bir çevrimiçi başvuru formu geliştirmişti, ancak geçen süre neredeyse hiç değişmedi.

Grup başkanı akışın her bölümünden insanları bir araya getiriyor: başvuru ekibi, iki teknik inceleyici, bir hukuk görevlisi, harç birimi ve izin belgelerini düzenleyen ekip. Başvuru tarihinden iznin başvurana ulaştığı tarihe kadar altı yakın tarihli izni haritalıyorlar. Sonuçlar ciddi. Toplam süre yaklaşık 110 gündü ve çalışma süresi yaklaşık 12. En uzun bekleme, başvuruların biri açmadan önce ortalama 40 gün beklediği teknik inceleme kuyruğundaydı ve başvuruların yaklaşık üçte biri yeniden istenmesi gereken eksik bilgiyle geliyordu. Harç birimi ve belge ekibi her biri toplu işleme için bir hafta bekleme ekliyordu.

Grup üç değişiklik üzerinde anlaşıyor. Çevrimiçi form, gönderimden önce yaygın biçimde eksik olan öğeleri kontrol ediyor. Teknik inceleme ekibi bir devam eden iş sınırı ve her başvuruyu eksiksizliği kontrol etmek için beş iş günü içinde açma kuralı koyuyor. Harç birimi ve belge ekibi haftalık partilerden günlük işlemeye geçiyor. Dijital hizmetler başkanını akış sahibi olarak adlandırıyor ve teslim süresini aylık gözden geçiriyorlar. Üç ay sonra medyan teslim süresi yaklaşık 70 gün ve eksik bilgi nedeniyle geri gönderilen başvuruların payı düşüyor. Bazı sorunlar sürüyor. İnceleme ekibi sınırın büyük, karmaşık başvuruları ele almayı zorlaştırdığını söylüyor ve hukuk görevlisi kimsenin saymadığı tek bir gecikme noktası. Akış sahibi inceleme ekibinden karmaşık vakaları kendi şeritlerine ayırmasını istiyor ve ikinci bir inceleyici için hukuk bürosuyla çalışıyor.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri akışın yalnızca bir kısmını görür. Haritalama oturumlarına katılın, verilerinizi paylaşın ve işin size ulaşmadan önce ve sizin yayımlamanızdan sonra ne olduğuna bakın. Akışın teslim süresini yalnızca kendi adımınızın değil, ortak bir hedef olarak görün.

### Hizmet ve operasyon ekipleri

En uzun kuyrukları çoğu zaman operasyon ekipleri tutar: erişim, onaylar, ortamlar, destek. Kapasiteniz ve kısıtlarınız konusunda açık olun. Haritayı, yukarı akıştaki ekiplerden eksiksiz girdi istemek ve önceliklerinizi açıklamak için kullanın.

### Liderlik ve yönetişim

Liderler, ekiplerin kaldıramayacağı ekipler arası kısıtları kaldırabilir. Akış sahipleri adlandırın, uçtan uca teslim süresini isteyin ve haritanın önerdiği iyileştirmelere yanıt verin. Dürüst veriyi caydıran akış ölçümlerini ekipleri sıralamak için kullanmaktan kaçının.

### Müşteriler ve kullanıcılar

Müşteriler ve kullanıcılar akışın tamamını deneyimler. Gecikmelerin nerede acıttığını ekibe söyleyin, başta eksiksiz bilgi verin ve davet edilirseniz bir haritalama oturumuna katılın. Talebin gerçekten ne zaman bittiğine dair görüşünüz akışın gerçek sonudur.

## Yaygın başarısızlık biçimleri

- **Tek bir ekibi optimize etmek.** Yerel kazanç uçtan uca hiçbir şeyi değiştirmez. Bunun yerine kısıtı bulun ve ele alın.
- **Hafızadan haritalamak.** Harita yöneticilerin inandığını yansıtır. Bunun yerine gerçek öğeleri gerçek tarihlerle izleyin.
- **Eksik sesler.** Tedarikçiler ve onaylayanlar odada değildir. Bunun yerine akıştaki her ekibi dahil edin.
- **Harita var, değişiklik yok.** Poster duvarda asılı kalır. Bunun yerine oturum bitmeden bir veya iki değişikliği sahipleriyle kararlaştırın.
- **Sahip olmaması.** Akıştan kimse sorumlu değildir. Bunun yerine toplama yetkisi olan bir akış sahibi belirleyin.
- **Sıralama olarak ölçümler.** Ekipler beklemeleri gizler. Bunun yerine ölçümleri akışı anlamak için kullanın ve açıkça tartışın.
- **Oynayan sınırlar.** İnsanlar boştayken WIP sınırları yükseltilir. Bunun yerine DORA'nın önerdiği gibi sınırları koruyun ve nedenleri düzeltin.
- **Önce araç.** Sorular bilinmeden bir pano satın alınır. Bunun yerine elle çizilmiş bir haritayla başlayın ve gerektikçe araç ekleyin.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Akışı görmek | Akış sezgiyle yargılanır | Bazı ekipler kendi adımlarını haritalar | Temel akışlar tüm ekiplerle gerçek öğelerden uçtan uca haritalanır | Teslim süresi, beklemeler ve doğruluk ölçülür ve gözden geçirilir | Akışlar kuruluşlar ve tedarikçiler arasında haritalanır ve ölçülür |
| Akışı iyileştirmek | Ekipler kendi adımlarını hızlandırır | Bazı ekipler arası değişiklikler denenir | Akış başına sahipli, kısıta odaklı bir iyileştirme listesi | İyileştirmeler ölçülen teslim süresine bağlanır ve kontrol edilir | Akış iyileştirme rutindir ve akışlar arasında paylaşılır |
| Sınırlar ve görünürlük | Devam eden iş sınırsız ve gizlidir | Bazı ekipler panolar ve sınırlar kullanır | İş ekipler arasında anlaşılmış sınırlarla görünürdür | Sınırlar teslim süresi verisiyle ayarlanır | Sınırlar ve görünürlük akışlar arasında eşgüdümlüdür |
| Sahiplik ve yönetişim | Akışın sahibi yoktur | Gayriresmî koordinatörler vardır | Her temel akışın adı belli bir sahibi ve düzenli bir gözden geçirmesi vardır | Sahipler ölçülen sonuçlardan sorumludur | Sahipler bütünü optimize etmek için akışlar arasında işbirliği yapar |

## Kontrol listesi

- [ ] Önemli bir akış seçtik ve gerçek öğelerden haritaladık.
- [ ] Harita her adımda çalışma süresini ve bekleme süresini gösteriyor.
- [ ] Akıştaki her ekipten insanlar haritalamaya katıldı.
- [ ] Uçtan uca teslim süresini ve ne kadarının bekleme olduğunu biliyoruz.
- [ ] Kısıtı belirledik ve bir veya iki değişiklik seçtik.
- [ ] Devam eden iş ekipler arasında görünür ve temel aşamalarda anlaşılmış sınırlar var.
- [ ] Adı belli bir kişi akışın sahibi.
- [ ] Kısa, düzenli bir gözden geçirme teslim süresine, beklemelere ve iyileştirme listesine bakıyor.
- [ ] Bir devirde işin ne sıklıkla eksik geldiğini izliyoruz.
- [ ] Akış ölçümleri ekipleri sıralamak için kullanılmıyor.

## Yapay zeka istemleri

**Amaç: gerçek öğelerden teslim süresini ve akış verimliliğini hesaplamak.**

```text
I have timing data for [number] recent items in the stream [name]. For each item and each step I have the date work began and ended, and the date it arrived at the step: [paste a table with real dates, step names, and the team responsible].

Using only my dates, calculate for each item the total lead time, the working time (end minus begin for each step), the waiting time (arrival at a step minus the end of the previous step), and the flow efficiency (working time divided by lead time). Show the average and range across items, and the three longest waits by team and step. Do not invent numbers. If dates are missing, say what to collect. List what you are unsure of.
```

**Amaç: bir değer akışı haritalama atölyesi planlamak.**

```text
Plan a 2-hour value stream mapping workshop for the stream [name].

Participants: [roles and teams].
Data to bring (real dates for [number] recent items): [describe what exists].
Constraints: [for example remote].

Provide a timed agenda: agree the start and end of the stream, walk through real items, mark steps with working time and waiting time, record rework and incomplete handovers, identify the constraint, draw a future state, and agree one or two changes with owners and dates. Include prompts to keep the conversation on the system. Keep it free of any particular tool. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: iki ekip arasındaki devir kalitesini çözümlemek.**

```text
Teams A and B hand work over in the stream [name]. Here are examples of items that came back for rework or information, with reason: [paste, one per line].

Group the reasons into categories using only the text. Count items per category from my list. For the top two categories, suggest an item for a handover checklist that team A could use, and a question for team B. Do not infer causes beyond the text. List what you are unsure of.
```

**Amaç: devam eden iş sınırı denemesi tasarlamak.**

```text
Design a four-week trial of work-in-process limits for [team] working in [stream or stage].

Current items in progress per person or stage: [paste real counts].
Lead time data we have: [describe].
Capacity, in people: [number].

Propose limits for each stage based on capacity, how to show work and age on a board, rules for pulling work, what to do when someone is idle (without raising limits), what to measure (leave targets as [to be agreed]), and what would make us stop. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Yapay zeka becerileri

- [value-stream-map](../../../../skills/value-stream-map/SKILL.md): bir akışı haritalamak, süreleri kaydetmek ve kısıtı bulmak için kullanın.
- [workflow-analysis](../../../../skills/workflow-analysis/SKILL.md): işin roller arasında nasıl hareket ettiğini ve nerede beklediğini incelemek için kullanın.
- [kanban](../../../../skills/kanban/SKILL.md): akış için görselleştirme ve devam eden iş sınırlarını kurmak için kullanın.
- [demand-analysis](../../../../skills/demand-analysis/SKILL.md): akışa neyin ve hangi hacimde girdiğini anlamak için kullanın.
- [portfolio-management](../../../../skills/portfolio-management/SKILL.md): hangi akışların ve girişimlerin yatırımı hak ettiğine karar vermek için kullanın.

## Temel kaynaklar

- **Value-stream mapping** (Wikipedia): mevcut durum ve gelecek durum haritalarının tanımı ve *Learning to See* kitabına bir işaret.
- **Work in process limits** (DORA, dora.dev): sınırları belirleme ve koruma ile yerel optimizasyondan kaçınma üzerine rehberlik.
- **The Kanban Guide** (kanbanguides.org): dört akış ölçümünün tanımları.
- **Lean software development** (Wikipedia): değer akışı düşüncesinin arkasındaki israflar ve ilkeler.

## Kaynakça

1. Value-stream mapping — Wikipedia — https://en.wikipedia.org/wiki/Value-stream_mapping
2. Work in process limits — DORA, dora.dev — https://dora.dev/capabilities/wip-limits/
3. Continuous delivery — DORA, dora.dev — https://dora.dev/capabilities/continuous-delivery/
4. The Kanban Guide — John Coleman, Daniel Vacanti, and contributors, kanbanguides.org — https://kanbanguides.org/english/
5. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
6. Lean manufacturing — Wikipedia — https://en.wikipedia.org/wiki/Lean_manufacturing
7. Kanban (development) — Wikipedia — https://en.wikipedia.org/wiki/Kanban_(development)
8. Theory of constraints — Wikipedia — https://en.wikipedia.org/wiki/Theory_of_constraints
9. Value chain — Wikipedia — https://en.wikipedia.org/wiki/Value_chain
