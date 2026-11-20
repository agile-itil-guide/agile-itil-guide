# Çevik Hizmet Yönetimi

**Çevik hizmet yönetimi, çevik değerleri ve yöntemleri hizmet yönetiminin kendisinin tasarımına ve iyileştirilmesine uygular; her süreci bir sahibi, bir iş listesi ve işleyip işlemediğini söyleyebilecek kullanıcıları olan bir ürün olarak ele alır.**

## Bu neden önemli

Bu kılavuzun büyük bölümü, çevik ekiplerin hizmet yönetimi uygulamalarını nasıl kullanabileceğine baktı. Bu konu soruyu tersine çevirir: hizmet yönetimi uygulamaları çevik biçimde nasıl oluşturulur ve değiştirilir? Birçok kuruluşun olaylar, değişiklikler ve talepler için bir kez tasarlanmış, bir projede devreye alınmış ve öylece bırakılmış süreçleri vardır. Bunlar değişmeye yavaştır, uymak zorunda olan insanlarca sevilmez ve kuruluşun artık yazılım geliştirme biçimiyle uyumsuzdur. Bu, Manifesto'nun değişimi memnuniyetle karşılama ilkesinin düşündüreceğinin tam tersidir (bkz. Konu 1.2 — Çevik İlkeler).

Çare, süreci bırakmak değil, onu kullanıcılarıyla birlikte tasarlanan, küçük adımlarla yayımlanan ve kanıttan iyileştirilen bir şey olarak ele almaktır. ITIL 4'ün yol gösterici ilkeleri de bunu söyler: bulunduğunuz yerden başlayın, geri bildirimle yinelemeli ilerleyin, işbirliği yapın ve görünürlüğü teşvik edin, sade ve pratik tutun (bkz. Konu 2.4 — ITIL Yol Gösterici İlkeleri). Wikipedia'daki ITIL maddesi, ITIL 4'ün 2019'da yayımlandığında çevik, DevOps ve yalın çalışma biçimleriyle uyumlu hale getirildiğini söyler. ISO/IEC 20000 maddesi bu standardın çevik ve DevOps üzerine rehberlik içeren yeni parçalarını sıralar, ancak içeriklerini vermez.

Çevik hizmet yönetimi üzerine başlı başına biçimsel araştırma azdır ve bu kılavuz için başvurulan Wikipedia maddeleri onu kapsamaz. Bu nedenle bu konu, Scrum Kılavuzu'nun roller ve yapıtlara ilişkin anlatımından, çevik ve ITIL ilkelerinden ve bu kılavuzun geri kalanından yararlanır ve yaklaşımını yerleşik bir yöntem olarak değil, denenecek pratik bir sentez olarak sunar.

## Temel kavramlar

### Ürün olarak süreçler

Bu anlamda bir **süreç**, bir hizmet kuruluşunun insanlardan izlemesini istediği her tekrarlanabilir çalışma biçimidir: bir olayın nasıl bildirileceği, erişimin nasıl talep edileceği, bir değişikliğin nasıl onaylanacağı. Ürün olarak görüldüğünde bir sürecin şunları vardır:

- **Kullanıcılar:** onu izleyen insanlar ve onun hizmet ettiği insanlar.
- **Bir amaç:** var olma nedeni olan sonuç.
- **Bir sahip:** değerinden sorumlu biri; tıpkı Scrum Kılavuzu'nun Ürün Sahibini ürünün değerini en üst düzeye çıkarmaktan ve iş listesini sıralamaktan sorumlu tek kişi olarak anlatması gibi (bkz. Konu 1.4 — Teslimat Tahmini ve Planlama Metrikleri).
- **Bir iş listesi (backlog):** iyileştirmelerin sıralı bir listesi.
- **Sürümler:** küçük adımlarla, notlarla birlikte teslim edilen değişiklikler.
- **Ölçümler:** işleyip işlemediğine dair kanıt.

Böyle düşünmek soruları değiştirir. "Değişiklik sürecini uyguladık mı?" değil, "değişiklik süreci insanların işini yapmasına yardımcı oluyor mu ve sonraki iyileştirme nedir?"

### Roller

| Rol | Bir ürün ekibinde | Bir hizmet yönetimi süreci için |
|---|---|---|
| **Ürün sahibi** | İş listesini sıralar ve değerden sorumludur | Sonra neyi neden iyileştireceğine karar veren süreç sahibi |
| **Geliştiriciler / ekip** | Artımı geliştirir | Süreci tasarlayan ve yürüten kişiler; ideal olarak teslimat ve operasyondan kullanıcıları da içerir |
| **Scrum Master veya koç** | Ekibin çerçeveyi uygulamasına yardım eder ve engelleri kaldırır | Ekibin sürekli yazılım teslimini uygulamasına ve geri bildirim toplamasına yardım eden bir koç |
| **Paydaşlar** | Artımı gözden geçirir ve geri bildirim verir | Teslimat ekipleri, hizmet masası, denetçiler, müşteriler |

Eşleme bu kılavuza aittir, bir standart değildir. Birçok kuruluşta süreç sahiplerinin yetkisi veya zamanı yoktur; bu nedenle ilk adım çoğu zaman onlara ikisini de vermektir.

### Süreç iş listesi

Bir süreç için iyileştirme fikirleri birçok yerden gelir: olay gözden geçirmeleri, retrospektifler, denetim bulguları, kullanıcı şikâyetleri ve ölçümler (bkz. Konu 3.15 — Sürekli İyileştirme). Bir süreç iş listesi bunları tek bir sıralı listede toplar. Maddeler küçüktür ve kullanıcının bakış açısından anlatılır: "Bir geliştirici olarak, hazır olduğumda yayımlayabilmek için düşük riskli değişikliklerin otomatik onaylanmasını istiyorum." Ürün sahibi listeyi değer ve çabaya göre sıralar, ekip de maddeleri kısa döngülere alır.

### Süreç değişikliklerinin sürekli yazılım teslimi

Tam bir süreç tasarlayıp devreye almak yerine, işleyebilecek en küçük sürümü tasarlayın, birkaç kullanıcıyla deneyin ve öğrenin:

| Adım | Ne olur |
|---|---|
| **Sorunu bulun** | İnsanların gerçekte nasıl çalıştığını ve nerede zorlandığını gözlemleyin |
| **Küçük bir değişiklik tasarlayın** | Yeni bir form, daha kısa bir onay yolu, bir kontrol listesi |
| **Deneyin** | Bir ekiple veya bir iş türüyle, kısa bir süre |
| **Kontrol edin** | Beklediğinizle karşılaştırın; veri ve konuşmadan yararlanın |
| **Benimseyin, ayarlayın veya bırakın** | İşe yarayanı yayın; yaramayanı düzeltin veya bırakın |

Bu, sürecin kendisine uygulanan planla–yap–kontrol et–önlem al döngüsüdür (bkz. Konu 3.15 — Sürekli İyileştirme).

### Kullanıcılarla tasarım

Süreci kullanmayan süreç tasarımcıları kaçınılabilir hatalar yapar. Süreci izleyen insanları dahil edin: değişiklik sürecini tasarlamak için mühendisleri, olay formunu tasarlamak için masa analistlerini ve talep kataloğunu tasarlamak için müşterileri davet edin. Gerçek işi izleyin. Gerçek vakalarla test edin. Bu, "sözleşme pazarlığı yerine müşteriyle işbirliği"nin kuruluşun içinde uygulanmasıdır (bkz. Konu 1.1 — Çevik Manifesto).

### Asgari uygulanabilir süreç

**Asgari uygulanabilir süreç**, amacı gerçekleştiren en küçük adım, kayıt ve rol kümesidir. Ona eklemek için bir gerekçe gerekir. "Sade ve pratik tut" yol gösterici ilkesi bunu destekler. Her adım için yararlı bir sınama, kaldırılırsa ne olacağını ve kimin fark edeceğini sormaktır. Yasayla veya sözleşmeyle gerekli kılınan denetimler kaynağı belirtilerek korunur; diğerleri sorgulanır.

### Süreç sürümleri ve iletişim

Bir süreç değiştiğinde insanların bilmesi gerekir. Değişiklikleri sürümler gibi ele alın: neyin değiştiğini, neden değiştiğini ve neyi farklı yapmak gerektiğini anlatan, sorular için bir irtibat kişisi bulunan kısa bir not. Küçük adımlarla, insanların izleyebileceği bir ritimle yayımlayın ve ekipleri büyük değişikliklerle şaşırtmaktan kaçının. Değişikliklerin görünür bir geçmişini tutun.

### Standartlar, denetimler ve çeviklik

Birçok kuruluşun standartları veya denetçileri karşılaması gerekir. ISO/IEC 20000 hizmet yönetim sistemleri için bir standarttır ve Wikipedia onun çevik ve DevOps üzerine rehberlik içeren yeni bir parçasını listeler (bkz. Konu 2.7 — BT Hizmet Yönetimi Çerçeveleri ve Standartları). Küçük adımlarla oluşturulan bir süreç, kayıtlar nasıl işlediğini ve nasıl değiştiğini gösteriyorsa denetimleri karşılayabilir: iş listesi, sürüm notları ve ölçümler kendileri kanıttır. Denetçilerle neye ihtiyaç duyduklarını erkenden konuşun ve çalışma biçiminizi onlara gösterin.

### Çevik hizmet yönetimi ve DevOps

Otomasyon ve hatlar gibi DevOps uygulamaları, süreçleri uygulamak için araçlardır (bkz. Konu 5.2 — DevOps). Bir süreç adımı, örneğin bir değişikliğin bir hattan kaydedilmesi gibi, otomatikleştirilebiliyorsa bunu yapın ve otomasyonu sürecin parçası sayın. Çevik hizmet yönetimi ve DevOps, kısa döngülere ve hızlı geri bildirime ortak ilgi paylaşır.

### Sınırlar

Yaklaşım, insanların süreci iyileştirmek için zamanı ve yetkisi olduğunu varsayar; bu her zaman doğru değildir. Süreç sahipliği göstermelik olduğunda, paydaşlar herhangi bir şey denemeden önce bitmiş bir tasarım talep ettiğinde veya her değişiklik uzun bir onay gerektirdiğinde başarısız olabilir. Değişiklikler insanların özümseyemeyeceği kadar sık olursa sürekli çalkantı riski de taşır. Sürekli değişiklik teslimini istikrarla dengeleyin: öngörülebilir bir ritimle değiştirin.

## İyi uygulamalar

1. **Her süreç için bir sahip belirleyin.** Onu değiştirme yetkisi ve bunu yapacak zamanı olan birini seçin. Rolünü netleştirin: sürecin amacına ne kadar iyi hizmet ettiğinden sorumludurlar.
2. **Tek cümlelik bir amaç yazın.** Sürecin ne için olduğunu ve kime hizmet ettiğini belirtin. Yapamıyorsanız süreç kaldırılmaya aday olabilir.
3. **Bir süreç iş listesi tutun.** Gözden geçirmelerden, denetimlerden, geri bildirimden ve verilerden gelen fikirleri tek bir sıralı listede toplayın. Süreci izleyen insanlara gösterin.
4. **Kullanıcıları tasarıma dahil edin.** Atölyelere ve denemelere mühendisleri, masa analistlerini ve müşterileri katın. Değiştirmeden önce gerçek işi gözlemleyin.
5. **Asgari uygulanabilir süreçle başlayın.** Amacı ve yasal gereksinimleri karşılayan en küçük sürümü tasarlayın. Adımları yalnızca bir sorun gerekçelendirdiğinde ekleyin.
6. **Devreye almadan önce deneyin.** Bir ekiple veya bir iş türüyle kısa, tanımlı bir süre pilot yapın. Başlamadan önce neye bakacağınızı kararlaştırın.
7. **Değişiklikleri bir ritimle küçük adımlarla yayımlayın.** Sürecin her sürümü için bir irtibat kişisiyle birlikte kısa bir not yayımlayın. Büyük, sürpriz değişikliklerden kaçının.
8. **Süreci ölçün.** İşleyip işlemediğine dair geçen süre, yeniden iş ve kullanıcı memnuniyeti gibi birkaç ölçüm seçin (bkz. Konu 5.6 — Metrikler ve Ölçüm). Bunları kullanıcılarla gözden geçirin.
9. **Yardımcı olduğu yerde otomatikleştirin.** Kayıtları formlardan değil araçlardan alın; kolay yolu doğru yol yapın. Otomasyonun, insanların vermesi gereken yargıyı gizlemediğini kontrol edin.
10. **Denetçiler için kanıtı saklayın.** İş listesini, kararları, sürüm notlarını ve ölçümleri denetçilerin görebileceği yerde saklayın. Onları sürecin nasıl değiştiğine dair bir gözden geçirmeye davet edin.
11. **Süreci emekliye ayırın.** Artık amacına hizmet etmeyen adımları, formları ve kayıtları kaldırın. Silmeyi bir iyileştirme olarak görün.
12. **Süreç sahipliğini yıllık gözden geçirin.** Her sürecin hâlâ etkin bir sahibi, güncel bir iş listesi ve ona ulaşabilen kullanıcıları olduğunu kontrol edin.

## Ekibinizle tartışılacak sorular

**Süreçlerimizin her birinin sahibi kim ve onu değiştirmek için ne kadar yetkisi var?**

Ana süreçleri listeleyin ve her biri için sahibi adlandırın. Sahibin kimseye sormadan neyi değiştirebileceğini sorun. Çoğu zaman yanıt "çok az"dır. Kolaylaştırıcı, sahibin küçük değişiklikleri hızla yapabilmesi için neyin gerektiğini sorabilir. Başlanacak bir süreçte anlaşın.

**Değişiklik sürecimiz ne için? Bunu tek cümleyle söyleyebilir miyiz?**

Herkesten bir amaç yazmasını isteyin. Karşılaştırın. Farklar sürecin neden var olduğuna dair kafa karışıklığını gösterir. Her adımı yargılamak için ortak ifadeyi kullanın. Ona hizmet etmeyen adımları kaldırın veya sorgulayın.

**Kullanıcılar istediği için bir süreci en son ne zaman değiştirdik ve bunu nasıl öğrendik?**

Örnekler isteyin. Hiç yoksa şikâyetlerin nereye gittiğini sorun. Geri bildirimin sahibe nasıl ulaşabileceğini tartışın: bir kanal, düzenli bir gözden geçirme, kısa bir anket. Denenecek bir yol seçin.

**Daha basit bir sürecin bir aylık denemesi nasıl görünürdü?**

Bilinen sürtünmesi olan bir süreç seçin. Daha hafif bir sürümü, kimin deneyeceğini, neyi ölçeceğinizi ve neyin sizi durduracağını anlatın. Bu bir tartışmayı bir deneye dönüştürür. Ayrıntılarda ve tarihte anlaşın.

**Sürekli yazılım teslimi yapan bir süreçten denetçilerimiz hangi kanıtı kabul ederdi?**

Bir denetçiye veya uyum meslektaşına sorun. Sürecin ürettiklerini listeleyin: bir iş listesi, sürüm notları, ölçümler, kayıtlar. Boşlukları tartışın. Ekipler, denetçilerin kontrollü değişikliğin net kanıtını kabul etmeye ne kadar istekli olduğuna çoğu zaman şaşırır.

**İnsanlar bir sürecin değiştiğini nasıl öğreniyor?**

Son değişikliğin izini sürün. Birçok kişi bir meslektaşından veya karşısına çıkarak öğrendi. Sürüm notlarını ve görünür bir değişiklik günlüğünü tartışın. Değişiklikleri duyurmanın basit bir yolunda ve nerede duracaklarında anlaşın.

## Uygulamada: çevik bir ITIL örneği

Ulusal bir trafik güvenliği kurumunun, polis ve mahkemelerin kullandığı bir uygulamayı destekleyen 90 kişilik bir BT departmanı var. Departmanın olay süreci sekiz yıl önce yazıldı: 14 alanlı bir form, yüksek öncelikli bir olayı kapatmak için üç onay ve kimsenin okumadığı aylık bir rapor. Teslimat ekipleri kesintiler sırasında formu atlıyor ve sonradan dolduruyor; bu yüzden kayıtları zayıf. Bir denetim bulgusu olay kayıtlarının eksik olduğunu söylüyor.

Hizmet yönetimi başkanı kendisini olay sürecinin sahibi olarak belirliyor ve küçük bir çalışma ekibi kuruyor: hizmet masasından iki analist, iki teslimat ekibinin her birinden bir mühendis ve kurumun yönetişim biriminden bir kalite görevlisi. Süreç için bir amaç yazıyor: hizmeti hızla eski haline getirmek ve olanlardan öğrenmek. Ekip üç gerçek olayı izliyor. Formun olaydan sonra, çoğunlukla aynı birkaç değerle doldurulduğunu ve onayların hiçbir sonucu değiştirmeden gecikme eklediğini görüyorlar. Bir iş listesi oluşturuyor ve en küçük değişikliklerle başlıyorlar. İki ekiple yapılan bir deneme formu, mümkün olduğunda izleme aracından otomatik doldurulan altı alana indiriyor, üç onaydan ikisini kaldırıyor ve her yüksek öncelikli olay için kısa bir suçlamasız gözden geçirme ekliyor.

Altı hafta sonra deneme ekipleri olayları sonradan değil kesinti sırasında kaydediyor ve kalite görevlisi kayıtları öncekinden daha eksiksiz buluyor. Ekip bir sayfalık bir sürüm notu yayımlıyor, değişikliği tüm ekiplere yayıyor ve denetçiye iş listesini, deneme sonuçlarını ve ölçümleri gösteriyor. Bazı zorluklar sürüyor. Bir teslimat ekibi denemeye hiç katılmadı ve hâlâ eski formu kullanıyor, bir tedarikçinin sözleşmesi yeni formun atladığı bir alanı gerektiriyor ve kalite görevlisi onayların kaldırılmasının bir sonraki denetimde sorgulanacağından endişe ediyor. Hizmet yönetimi başkanı tedarikçi durumu için bir alan ekliyor, kalan ekibe sonraki tura katılmasını istiyor ve denetçiyle olay kayıtlarını bir sonraki üç aylık toplantıda gözden geçirmek üzere anlaşıyor.

## Dört bakış açısı

### Ürün ve teslimat ekipleri

Teslimat ekipleri birçok hizmet yönetimi sürecinin kullanıcılarıdır. Sizi etkileyenlerin tasarımına katılın, uygulamada nasıl işlediklerine dair veri sunun ve pilotları deneyin. Bir süreç adımı hattınızda otomatikleştirilebiliyorsa bunu geliştirmeyi önerin.

### Hizmet ve operasyon ekipleri

Süreçlerin sahibi çoğu zaman operasyon ekipleridir. Her birini bir ürün olarak ele alın: bir amaç yazın, bir iş listesi tutun, kullanıcılara sorun ve küçük değişiklikleri yayımlayın. Süreç iyileştirmesine zaman ayırın ve bunu savunun; çünkü teslimat işi onu sıkıştıracaktır.

### Liderlik ve yönetişim

Liderler süreç sahiplerine yetki ve zaman verir ve süreçlerin kanıttan değiştiği beklentisini belirler. Her sürecin amacını ve ölçümlerini, bir de iş listesini isteyin. Denemeleri destekleyin ve kanıtı yeni biçimlerde kabul etmeye istekli olun.

### Müşteriler ve kullanıcılar

Hizmetlerin müşterileri ve kullanıcıları da talepler ve onaylar gibi süreçleri izler. Sahibe neyin kafa karıştırıcı veya yavaş olduğunu söyleyin. Bir denemeye katılmayı önerin. Değişikliklerin duyurulmasını ve açıklanmasını bekleyin.

## Yaygın başarısızlık biçimleri

- **Sahibi olmayan süreç.** Kimse değiştiremez. Bunun yerine yetkisi ve zamanı olan bir sahip belirleyin.
- **Büyük patlama yeniden tasarımı.** Tüm yeni bir süreç bir seferde devreye alınır ve reddedilir. Bunun yerine küçük adımlarla değiştirin ve pilot yapın.
- **Kullanıcılardan uzak, komiteyle tasarım.** Süreç tasarımcılara uygun olur. Bunun yerine onu izleyen insanları dahil edin ve gerçek işi gözlemleyin.
- **Sürekli çalkantı.** Değişiklikler özümsenemeyecek kadar sık gelir. Bunun yerine öngörülebilir bir ritimle yayımlayın.
- **Yasal gereksinimleri unutmak.** Gerekli bir denetim bırakılır. Bunun yerine her adımın ne için gerekli olduğunu kontrol edin ve kaynağı belirtin.
- **Duyurulmayan değişiklikler.** İnsanlar bunları tesadüfen keşfeder. Bunun yerine kısa sürüm notları yayımlayın.
- **Kanıtın saklanmaması.** Denetim sürecin nasıl değiştiğini göremez. Bunun yerine iş listesini, kararları ve ölçümleri saklayın.
- **Kaldırma olmaması.** Adımlar birikir. Bunun yerine silmeyi bir iyileştirme olarak görün.

## Olgunluk modeli

| Boyut | Başlangıç | Gelişim | Standartlaştırma | Yönetim | Eşgüdüm |
|---|---|---|---|---|---|
| Sahiplik ve amaç | Süreçlerin net bir sahibi veya amacı yoktur | Bazı süreçlerin sahipleri vardır | Her sürecin yetkili bir sahibi ve yazılı bir amacı vardır | Sahipler etkililik açısından gözden geçirilir ve desteklenir | Sahipler süreçleri uçtan uca hizalamak için ekipler arasında birlikte çalışır |
| İş listesi ve değişiklik | Değişiklikler nadir ve büyük projelerdir | Bazı sahipler fikir listeleri tutar | Her sürecin sıralı bir iş listesi vardır ve değişiklikleri küçük adımlarla yayımlar | İş listesi akışı ve sürüm etkileri ölçülür | Süreç değişiklikleri süreçler arasında ve tedarikçilerle eşgüdümlüdür |
| Kullanıcıları dahil etme | Tasarımcılar kullanıcılara nadiren danışır | Bazı denemeler kullanıcılarla yapılır | Kullanıcılar tasarım ve denemelere standart olarak katılır | Kullanıcı geri bildirimi ve memnuniyeti ölçülür ve buna göre harekete geçilir | Müşteriler ve tedarikçiler süreç tasarımına katılır |
| Kanıt ve denetim | Kayıtlar zayıftır ve değişiklikler kaydedilmez | Bazı süreç değişiklikleri günlüğe alınır | İş listesi, sürüm notları ve ölçümler denetim kanıtı olarak hizmet eder | Denetçiler değişiklik kaydını düzenli gözden geçirir | Kanıt denetçiler ve ortaklarla sürekli paylaşılır |

## Kontrol listesi

- [ ] Her ana sürecin yetkisi ve zamanı olan adı belli bir sahibi var.
- [ ] Her sürecin tek cümlelik bir amacı ve tanımlı bir kullanıcı kümesi var.
- [ ] Her sürecin görünür, sıralı bir iyileştirme iş listesi var.
- [ ] Teslimat ve operasyondan kullanıcılar tasarım ve denemelere katılıyor.
- [ ] Değişiklikler devreye almadan önce, tanımlı bir kontrolle pilot ediliyor.
- [ ] Süreç değişiklikleri bir ritimle, kısa notlarla yayımlanıyor.
- [ ] Birkaç ölçüm her sürecin işleyip işlemediğini gösteriyor.
- [ ] Yasal ve sözleşmesel denetimler kaynaklarıyla birlikte belirlenmiş.
- [ ] Denetçiler iş listesini, sürüm notlarını ve ölçümleri gördü.
- [ ] Artık bir amaca hizmet etmeyen adımlar kaldırılıyor.

## Yapay zeka istemleri

**Amaç: bir süreç için amaç ifadesi ve kullanıcı listesi taslağı hazırlamak.**

```text
Help me write a purpose statement for this process: [name and brief description].

Who follows it: [roles].
Who it serves: [roles].
What goes wrong today: [examples].
Rules or contracts that require parts of it, with source text: [paste, or write "none known"].

Write three alternative one-sentence purpose statements, each focused on an outcome and not on the steps. Then list questions for the users to test which is closest. Do not invent rules. Ask clarifying questions first, and list what you are unsure of.
```

**Amaç: geri bildirimi ve olay gözden geçirmelerini bir süreç iş listesine dönüştürmek.**

```text
Here are comments, complaints, audit findings, and review actions about [process]: [paste one per line, with source].

Group related items. For each group, write a backlog item in the form "As a [role], I want [change] so that [outcome]," using only what the text says. Add a note on who is affected and a question about evidence. Leave priority blank. List items that look like requirements from law or contract, quoting the text, and items that conflict. List what you are unsure of.
```

**Amaç: daha hafif bir sürecin bir aylık denemesini tasarlamak.**

```text
Design a one-month trial of a lighter version of [process].

Current steps and where people struggle: [describe].
Proposed change: [describe].
Teams that could take part: [list].
Controls that must stay, with source: [list, or write "none known"].

Give: the trial scope, what we expect to see, what to measure before and during (leave targets as [to be agreed]), how to gather user feedback, conditions to stop, and what evidence to keep for auditors. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Amaç: bir süreç değişikliği için sürüm notu yazmak.**

```text
Write a short release note for a change to [process].

What changed: [describe].
Why: [describe].
Who is affected and from what date: [describe].
What people should do differently: [describe].
Where to ask questions: [contact].

Write under 150 words in plain language, with a heading, a short list of changes, and what to do. Use only my information. Ask clarifying questions first if anything is missing, and list what you are unsure of.
```

## Yapay zeka becerileri

- [raci-matrix](../../../../skills/raci-matrix/SKILL.md): her sürecin sahibinin kim olduğunu ve kime danışıldığını netleştirmek için kullanın.
- [user-story](../../../../skills/user-story/SKILL.md): süreç iş listesi maddelerini kullanıcının bakış açısından yazmak için kullanın.
- [workflow-analysis](../../../../skills/workflow-analysis/SKILL.md): bir sürecin gerçekte nasıl işlediğini ve nerede zorlandığını incelemek için kullanın.
- [agile-reflection](../../../../skills/agile-reflection/SKILL.md): bir sürecin kullanıcılarıyla birlikte nasıl işlediğini gözden geçirmek için kullanın.
- [kaizen](../../../../skills/kaizen/SKILL.md): bir sürece küçük, sürekli iyileştirmeler planlamak için kullanın.

## Temel kaynaklar

- **The Scrum Guide** (Ken Schwaber ve Jeff Sutherland, scrumguides.org): süreç sahipliği ve iş listeleri için analoji olarak burada kullanılan rollerin ve yapıtların kaynağı.
- **Principles behind the Agile Manifesto** (agilemanifesto.org): tasarım yaklaşımının çevik yönü.
- **ITIL** (Wikipedia): ITIL 4'ün çevik, DevOps ve yalın çalışma biçimleriyle uyumlandırılmasının tarihçesi.
- **ISO/IEC 20000** (Wikipedia): çevik ve DevOps üzerine yeni rehberlik dahil parçaların listesi.

## Kaynakça

1. The Scrum Guide (November 2020) — Ken Schwaber and Jeff Sutherland, scrumguides.org — https://scrumguides.org/scrum-guide.html
2. Principles behind the Agile Manifesto — Beck et al., agilemanifesto.org — https://agilemanifesto.org/principles.html
3. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
4. ISO/IEC 20000 — Wikipedia — https://en.wikipedia.org/wiki/ISO/IEC_20000
5. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
6. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
7. PDCA — Wikipedia — https://en.wikipedia.org/wiki/PDCA
8. Business process management — Wikipedia — https://en.wikipedia.org/wiki/Business_process_management
9. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
