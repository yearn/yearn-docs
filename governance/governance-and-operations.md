# Yönetim ve İşleyiş

[YIP-61: Governance 2.0](https://gov.yearn.finance/t/yip-61-governance-2-0/10460) 25 Nisan 2021'de geçtiğinden beri, Yearn **multi-DAO** yapısı, **kısıtlı yetkilendirme** ile yönetilir. Bu yaklaşım, protokol geliştirmenin yeterli düzeyde ademi merkeziyetçiliği korurken bürokrasi tarafından katılaştırılmamasına izin verir.

Multi-DAO, protokole benzersiz bir şekilde katkıda bulunan merkezi olmayan özerk kuruluşların (DAO'lar) değişken sayısını ifade eder. Bu bağımsız gruplar YFI sahipleri, yTeams ve Multisig'den oluşur.

- **YFI sahipleri** protokol veya protokol yönetim yapısındaki değişiklikler için oy verir
- **yTeams** protokolün veya ilgili işlemlerin belirli yönlerine odaklanır
- **Multisig** üyeleri zincirle ilgili kararları uygular veya veto eder

Token sahipleri, Multisig'in bir parçası olan yTeams'in ne olduğu ve her grubun operasyonel kontrolünün sınırlamaları hakkında nihai söz hakkına sahiptir. 'Kısıtlı yetkilendirme' terimi, Yearn'i oluşturan ve yöneten çeşitli gruplara belirli yetkiler veren token sahiplerinden kaynaklanmaktadır.

Basitleştirilmiş bir yönetişim akışı şöyle görünür:

    1. YFI sahipleri, yTeams'in sınırlarını yaratır, yok eder ve tanımlar
    2. yTeam bir kararı yTx'e bildirir
    3. yTx, yetki verilmiş bir işlem oluşturur ve bunu Multisig'e gönderir
    4. Multisig işlemi yürütür veya veto eder
    
## DAO Yükümlülükleri

![](https://i.imgur.com/IDysF5O.png)

### Token Sahipleri

protokolü geliştiren teklifleri oluşturmak ve oylamak YFI sahibinin görevidir.

| Öneriler | Tanımlar |
|----------|----------|
|İyileştirme Önergesi (YIP)|YFI sahiplerine devredilen veya sayılan yetkilerin kapsamı dışında kalan herhangi bir yetki üzerinden yürütme önerisi|
|Yearn Heyet Önergesi (YDP)|Herhangi bir ayrık karar verme yetkisinin devredildiği yerde değişiklik önerisi|
|Yearn Sinyalizasyon Önergesi (YSP)|Herhangi bir konuda topluluk duygularını veya niyetini belirtmek için bağlayıcı olmayan bir öneri|

Spesifik olarak, bu öneriler, token sahiplerinin aşağıdaki kararları almasına izin verir:

| Yetki | Tanım |
|-------|-------------|
|Yetki Yönetimi|YFI sahipleri, yTeams'e veya yTeams'den ayrı yetkiler oluşturmak, atamak veya iptal etmek için oy kullanabilir|
|YFI Token Sözleşmesini Değiştirmek|YFI token sözleşmesiyle, YFI basımı veya basım anahtarlarını yakmak gibi herhangi bir etkileşim, YFI sahiplerinin kontrolü altında kalır.|
|Ücretleri Belirlemek|Yearn Protokolünde standart ücret yapılarını belirlemek|
|Multisig yetkililerini Değiştirmek|Multisig yakın vadede kritik yetkileri elinde tutmaya devam edeceğinden, imzalayanları değiştirmek için yalnızca YFI sahipleri oy kullanabilir|
|yTeams'i onamak|Hangi yTeams'in devredilen yetkileri elinde tutabileceğini kontrol etmek için yTeams'i resmi olarak onamak veya yadsımak|
|yOps İmza yetkililerini Değiştirmek|yOps, diğer yTeam imza yetkililerini değiştirme gücüne sahip olduğundan, bu, yOps'un imza yetkililerini değiştirmeye yönelik özel bir gücüdür.|
|hazine fonlarını harcamak|Hazineden sağlanan Fonlarını Harcamak|
|YIP Yetkisi|YFI Sahipleri, halihazırda devredilmemiş herhangi bir konuda YIP öneri yetkisine sahiptir|
### yTeams

Her yTeam, token sahipleri tarafından tanımlanan nesnel ve ayrı yetkilere sahiptir.Bunlar, kapsayıcı ekiple benzer hedeflere yönelik çalışan ayrı katılımcı grupları olan üyelik havuzlarına daha da ayrılabilir.Ek olarak, bir üyelik havuzu birden fazla yTeam'in parçası olabilir.

| yTeam | Hedef | Üyelik Havuzu |
|-------|-----------|-----------------|
|yGuard|Vault'ların korur|YFI Protokol Geliştiricileri, YFI Stratejistleri, YFI Mekaniği, YFI Gizli Hayranları|
|yBrain|Stratejileri yönetir|YFI Stratejistleri|
|yDev|Protokolü yönetir |YFI Protokol Geliştiricisi|
|yPeople|Takımı yönetir|Ödemeleri Yapan YFI Çalışma Ekibi, YFI Danışmanları|
|yBudget|Harcamaları iyi yapar|YFI Finansları, YFI Danışmanları|
|yFarm|Hazineyi büyütür |YFI Gizli Hayranları, YFI Gizli Giriş|
|yTx|Muameleleri yazar|YFI Yapanlar|
|yOps|İştirakçiları koordine eder|YFI Operasyonları|

Her yTeam'e, YIP-61 tarafından tanımlanan belirli karar verme yetkileri verilir:

| yTeam | Yetki | Tanım |
|-------|-------|-------------|
|yGuard|Acil Durum Yetkiler|Stratejileri kapatma veya çökertme,vaut'lara saldırı veya hata durumunda anında müdahale eder|
|yBrain|Stratejileri etkinleştirir, devre dışı bırakır, ayarlar ve sürdürür|
|yDev|Yearn Protokolünü Tanımlar|DHangi kodun yearn'in bir parçası olarak kabul edilip edilmediğine karar verir|
|yDev|Protokolü Yönet|Yearn Protokolünü sürdürmek ve geliştirmek|
|yDev|Strateji Ekler|Vault'lara yeni stratejiler ekler|
|yTx|İşlemleri Delege Eder|Multisig'in imzalaması ve yürütmesi için temsilci işlemler oluşturur|
|yPeople|Ödeme Ekibi|Yearn ödeme paketleri oluşturur, dağıtır, değiştirir veya sonlandırır|
|yBudget|Bütçeleri Belirler|Koordinasyon, hibeler, işe alma, operasyonlar veya diğer iş akışları için bütçeler oluşturur|
|yFarm|Farm Hazinesi|Hazine ile Farm yapar ve bedelsiz dağılımlarla ilgili kararlar alır|
|yOps|yTeam İmza yetkililerini Onaylar|Resmi olaraker yTeam için imza yetkililerini onaylar veya kaldırır|

### Multisig

yTeams tarafından verilen kararlar, uygulama için daha merkezi olmayan bir sistem onaylanana kadar Multisig tarafından zincir üzerinde yürütülür. Bu arada[Multisig](https://docs.yearn.finance/resources/faq#who-is-on-the-multisig) şunları kontrol eder:


| Yetki | Tanım |
|-------|-------------|
|İcra Yetkisi|YFI sahipleri ve zincir-içi yTeams tarafından verilen kararları uygulama gücü|
|Veto Yetkisi|Bu yetki, Multisig'in herhangi bir kararı veto etmesine izin verir ve ideal olarak buna ihtiyaç duyulmamalıdır|
|Geçici Yetki|Multisig'in, karar verme yetkilileri gerekli tüm işlemleri yapana kadar YIP-41'in yetkisi altında çalışmasını sağlayan geçici bir yetki|


## Gelecekteki Uygulamalar

Yearn, DAO ademi merkeziyetçiliği ve üretkenlik arasında ideal bir dengeye giden yolu sürekli olarak açıyor.Çabaların şimdiki safhası, çoğunlukla sosyal katmanda değişiklikler gerektiriyor ve gelecekte aşağıdakiler gibi yazılım uygulamalarına doğru ilerleyeceğiz:

- Her yTeam'in yürütme gücüne sahip olmasını sağlayan çoklu imza konsensüs mekanizmaları
- Vekaleten oy kullanmadan zincir içi oylamaya geçiş
- karar verme yetkilerini NFT'lar olarak sınıflandırmak
- Bütçe tahsisi ve tazminat gibi şeyler için [Coordinape](https://coordinape.com/)'i kullamak


