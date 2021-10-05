# Genel Bakış

## yVault'lar nedir?

[yVault'lar](https://yearn.finance/vaults), kripto varlıklarınız için tasarruf hesapları gibidir. Depozitonuzu kabul ederler, ardından DeFi'de mevcut olan en yüksek verimi sağlayan bir stratejiye yönlendirirler.

![](https://i.imgur.com/yXnJqsn.png)

## Herhangi bir aktifle takas edin

[Zapper](https://zapper.fi/) sayesinde yVault'lara para yatırmak son derece kolaydır. %1'den daha az slipajla  Uniswap'ta takas edilebilecek bir token'iniz olduğu sürece, vault token'i kabul edecek, vault için gerekli olana dönüştürecek ve hepsini aynı işlemde yatıracaktır.

Geri çekerken, kullanıcılar aşağıdaki token'lardan birile tekrar takas edebilirler:
- ETH, WETH, DAI, USDT, USDC, WBTC

## yVault Ücretlendirme Yapısı

|yVault Sürümü|Çekme Ücreti|Performans Ücreti|Yönetim Ücreti|
|--------------|:-----------:|:-------------:|:------------:|
|v1|0.5%|5%|-|
|v2|-|20%|2%|

**Para Çekme Ücreti**: Çektiğinizde bakiyenize bir kerelik ücret yansıtılır. Bu, tüm vault'lar için kapatıldı ve yalnızca v1 yinelemesinde mevcuttu.

**Performans Ücreti**: Bir vault bir stratejiyi her hasat ettiğinde kazanılan verimden düşülür.

**Yönetim Ücreti**: Bir yıl boyunca vault mevduatlarından alınan sabit oran. Ücret, vault'un yeni hisselerinin basılmasıyla elde edilir, böylece vault katılımcıları seyreltilir. Bu, hasat zamanında yapılır ve önceki hasattan bu yana geçen süreye göre hesaplanır.

Örneğin, bir kasa günde ortalama olarak mevduatın yaklaşık %0,0055'ini alır (2 (yüzde)/365 (gün)):
- Hasat yapıldıktan 5 gün sonra vault token'larını % 5 * .0055 oranında seyreltir
- 7 gün boyunca gerçekleşmemiş olsaydı, bir sonraki hasatta vault token'larını %7 * .0055 oranında seyreltirdi
- - Vault'lar, yalnızca ücretlerden sonra kârlıysa hasat eder, böylece kullanıcılar yatırdıkları depozitodan daha azını çekmez

[yearn.finance](https://yearn.finance/) kullanıcı arayüzünde getiri net APY olarak görüntülenir. Bu, sunulan oranlarda hem ücretlerin hem de bileşik getirilerin dikkate alındığı anlamına gelir. Hasatlar belirli bir temelde gerçekleşmediğinden, verim geçmiş verilere dayalı olarak tahmin edilmektedir. Detaylı bilgi için bkz. [yVault YG'yi Anlama](https://docs.yearn.finance/resources/guides/how-to-understand-yvault-roi)

## v2 yVault İyileştirmeleri

- **Vault başına 20 stratejiye kadar:** Bu, farklı piyasa senaryolarında sermayeyi verimli bir şekilde yönetme esnekliğini artıracaktır. Her stratejinin bir sermaye sınırı vardır. Bu, artık APY'yi artıramayacak bir stratejiye aşırı fon tahsis etmekten kaçınmak için yararlıdır.
- **Stratejistler ve Guardian yeni Kontrolörlerdir:** kontrolör konsepti V2 yVaults'ta mevcut değildir ve yerini bir Guardian ve Strateji oluşturucu \(stratejist\) almıştır.
- Bu 2 aktör, strateji performansını denetler ve sermaye yönetimini iyileştirmek veya kritik durumlarda eyleme geçmek için  harekete geçme yetkisine sahiptir.
- **Otomatik Vault temizliği \(Keep3r ağı\):** `harvest()` ve `earn()` çağrıları artık Keep3r bot ağı üzerinden otomatik hale getirildi. Bu 2 işlev çağrısı, kazançları kasaya ve daha sonra stratejilere geri taşırken kazanılan token'leri satarak yeni temel teminat satın almak için kullanılır. Keep3r ağı, bu çağrıları yapmanın ve gaz maliyetleriyle birlikte çalışmanın ağır yükünü keep3r token'leri karşılığında alır. Bu tutum, insanları ek işlemlerden kurtarır. 
- **Koruma ve Davetli listeleri**: Yearn, yeni vault'lar için benzersiz bir geliştirme süreci yarattı. Başlangıç için tüm vault'lar Test vault'ları \(tyvToken\) olarak başlatıldı. Test vault'larının ve dolayısıyla stratejilerinin de bir üst sınırı vardır. Ayrıca, Koruma, Test Vault'larına para yatırarak ve çekerek etkileşimde bulunabilen bir misafir cüzdan listesine sahiptir. Bu tutum, bilgisiz kullanıcıların üretime hazır olmayan bir üründe potansiyel olarak para kaybetmelerini önler.
