# Using Yearn       

'zap' adı verilen bir özellik sayesinde, hemen hemen her token ile herhangi bir vault'a para yatırmak son derece kolaydır.

Nasıl çalıştığına bakalım:

Birinci, sağ üst köşedeki **Connect your wallet** düğmesini kullanarak Cüzdanınızı bağlayın. Birden fazla soğuk cüzdan desteklenir fakat insanlar çoğunlukla chrome’un uzantısı olup apple ve android storedan ücretsiz indirilebildiği için [MetaMask](https://metamask.io/) kullanmayı tercih ediyor. Cüzdanınızın Ethereum ağına bağlı olduğundan emin olun.

<p align="center">
  <img width="1266.75" height="345.75" src="https://i.imgur.com/H0Uc8e8.png">
</p>

## Eğer elinizde yatırım yapacağınız vault için gerekli olan token varsa:

1\. yatırım yapmak istediğiniz vault'u seçin

2\. Valult'a yatırmak istediğiniz token miktarını girin ETH yatıracaksanız, bir sonraki yapacağınız işlem için ihtiyacınız olacak işlem bedeli kadar ETH’i hesabınızda tuttuğunuzdan emin olun.

<p align="center">
  <img width="914.26" height="360.75" src="https://i.imgur.com/LGdRAMQ.png">
</p>

3\. Daha önce onaylayıp onaylamadığınıza bağlı olarak 'Onayla(Approve)' veya 'Para Yatır(Deposit)' düğmesini tıklayın.

4\. Cüzdanınız sizden işlemi onaylamanızı isteyecektir. Bu yaklaşık 3 dakika sürecektir, ancak işlemi [daha yüksek bir gaz bedeli](https://blog.leverj.io/how-to-set-the-gas-limit-and-gas-price-in-metamask-1b33c38c32fd) ödeyerek hızlandırabilirsiniz. İşleminiz takılı kalırsa, işlemi hızlandırmak veya iptal etmek için [bu kılavuza](https://metamask.zendesk.com/hc/en-us/articles/360015489251-How-to-Speed-Up-or-Cancel-a-Pending-Transaction) bakın.

<p align="center">
  <img width="258.75" height=" 459.75" src="https://i.imgur.com/BkXBANS.png">
</p>

5\. işleminiz gerçekleştiğinde yatırım yaptığınız vault ilk sıraya yükselecektir ve yatırdığınız meblağ vault’unuzu ara yüzünde görünecektir.

<p align="center">
  <img width="928.5" height="93.75" src="https://i.imgur.com/JvNQ3l2.png">
</p>

Yatırdığınızı geri çekmeye hazır olduğunuzda:

1\. Çekme işlemini yapmak istediğiniz vault’u seçin.

2\. Çekmek istediğiniz tutarı girin veya tüm bakiyeyi çekmek için 'Max' seçeneğine tıklayın.

<p align="center">
  <img width="910.5" height="361.5" src="https://i.imgur.com/Y3NsCRb.png">
</p>

3\. 'Withdraw'ı tıklayın.

4\. Cüzdanınız sizden işlemi onaylamanızı isteyecektir. Detaylı bilgi için yukarıdaki 4.adıma bakın.

5\. İşleminiz gerçekleştiğinde tokenlar tekrar cüzdanınızda görünecektir.

## Eğer elinizde yatırım yapacağınız vault için **gerekli olan token yoksa**

Bu yaygın bir durum olabilir, çünkü Yearn vaultlarının çoğu, [Curve Finance](http://curve.finance/)'a yatırım yaparak elde edilen liquidity provider(likuidite sağlayıcı) (LP) token'leri ile getiri sağlar.

Örneğin, daha yüksek kar payı için ETH vault yerine crvSTETH vault’a para yatırmayı tercih ediyorsanız ve Curve havuzlarının ve ETH türevi token'lerin(STETH) barındırdığı riski kabul ediyorsanız ama cüzdanınızda sadece ETH varsa vault’a eklemeden önce STETH token’a dönüştürmeniz gerekir.

Neyse ki Yearn'in 'zap' özelliği sayesinde, tüm bu para yatırma işleminiz tek seferde yapılabilir. Örnek olarak crvSTETH Vault'unun nasıl çalıştığı aşağıda açıklanmıştır:

**NOT:** Vault'a yatırmak üzere her hangi bir token'ı dönüştürmek(zap etmek), vault'un kendi yerel token'ını yatırmaktan daha fazla işlem gerektirir. Bu, token’ın takas edildiğinde veya bir havuza yatırıldığında daha fazla gaz ödeyeceğiniz ve potansiyel olarak slipajdan dolayı token’ın değer kaybedeceği anlamına gelir. Yearn slipajı %1 ile sınırlar ve slipaj bunu aşarsa işlem başarısız olur, bu durumda token'ları manuel olarak takas etmeniz veya yatırmanız gerekir. Ayrıntılı bilgi için [zap](https://docs.yearn.finance/yearn-finance/yvaults/overview#zap-in-with-any-asset) bölümümüze bakın.

1\. crvSTETH kasasını seçin.

2\. 'Approve' veya 'Deposit' düğmesinin yanındaki açılır kutuyu tıklayın.

3\. crvSTETH'e dönüştürülmesini istediğiniz token'ı seçin. Yalnızca cüzdanınızdaki token'nları gösterir.

<p align="center">
  <img width="909" height="363" src="https://i.imgur.com/6K1luO7.png">
</p>

4\. Yatırmak istediğiniz token miktarını girin ve token'ı daha önce onaylayıp onaylamadığınıza bağlı olarak 'Approve' veya 'Deposit' seçeneğine tıklayın.

5\. İşlemi cüzdanınızdan onaylayın. Daha fazla ayrıntı için yukarıdaki bölümdeki 4. adıma bakın.

6\. işleminiz gerçekleştiğinde yatırım yaptığınız vault ilk sıraya yükselecektir ve yatırdığınız meblağ vault’unuzu ara yüzünde görünecektir.

Yatırdığınızı geri çekmeye hazır olduğunuzda:

1\. crvSTETH vault'unu seçin.

2\. 'Withdraw' düğmesinin yanındaki açılır kutuyu tıklayın.

<p align="center">
  <img width="915.75" height="600.75" src="https://i.imgur.com/2UyXKN0.png">
</p>

3\. Çektiğinizde hangi token'ı almak istediğiniz seçin. Seçenekleriniz crvSTETH, ETH, BTC, DAI, USDC veya USDT olacaktır.

4\. Çekmek istediğiniz tutarı girin veya tüm bakiyeyi çekmek için 'Max' seçeneğine tıklayın.

5\. Gerekirse onayı kabul edin ve ardından para çekme işlemini onaylayın.

6\. İşleminiz gerçekleştiğinde tokenlar tekrar cüzdanınızda görünecektir.

## Fonlarınızı takip etmek için araçlar

Varlıklarınız bir Vault’tayken USD bakiyenizin nasıl değiştiğini görmek istiyorsanız, cüzdanınızı [zapper.fi](https://zapper.fi) veya benzer bir portföy izleme ürünlerine bağlayın. Bu, Vault'un sizin için ne kadar kâr getirdiğini de söylemenin en kolay yoludur.

Bakiyeniz sürekli olarak ARTMAYACAKTIR. Kar, dalgalı bir temelde gerçekleşen hasat() işlevi çağrıldığında kasadaki payınıza dağıtılacaktır.

Geri dönüşleri takip edebilmek için topluluk kaynakları:

- [Zapper](https://zapper.fi/)
- [Zerion](https://app.zerion.io/)
- [Yearn Vault ROI Calculator](https://yearn-roi.xyz/#/)
- [yVault ROI](https://yvault-roi.netlify.app/)
- [https://trackavault.com/](https://trackavault.com/)
