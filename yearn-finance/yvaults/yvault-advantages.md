# Yearn veriminizi nasıl artırır

yVaults'un etkileşimde bulunduğu hemen hemen her şey halka açıktır. Peki Yearn, kullanıcılara kendi başlarına elde edebileceklerinden daha iyi bir getiriyi nasıl sunabilir?

## Curve Finance'nin Sinerjisi

Yearn'in stratejilerinin çoğu, Curve Finance'in likidite madenciliği programını kullanır. [Curve Finance](https://curve.fi/), düşük slipajlı merkezi olmayan borsalarında likidite sağlayanlar için 300 yıllık bir token dağıtım programına sahiptir.

### veCRV Güçlendirmeleri

CRV, Curve [gauge](https://resources.curve.fi/base-features/understanding-gauges)'nin içinde belirli likidite sağlayıcı token'i stake eden kullanıcılara sürekli olarak dağıtılır. Bu CRV ödülleri, kullanıcı CRV'lerini [Locker](https://dao.curve.fi/locker)'da kilitlediğinde artırılabilir. Bu locker, karşılığında, hissedarlara yönetimde oy kullanma ve protokol ücretlerinin bir kısmını talep etme hakkını taşıyan  veCRV'yi verir.

CRV'yi kilitlemek, kullanıcıların uygun havuzlara likidite sağlarken aldıkları CRV ödüllerini artırmalarına olanak sağlar.Artış miktarı, ne kadar CRV'nin kilitlendiğine ve havuzdaki göreceli paylarına göre belirlenir.

![](https://i.imgur.com/QaMMdr7.png)

Yearn, Backscratcher yVault'u kullanarak önemli miktarda CRV'yi süresiz olarak kilitler ve güçlendirmeleri çeşitli yVault'lara dağıtır.  

### Backscratcher yVault

Backscratcher yVault, hem Curve hem de Yearn için faydalı olacak şekilde likidite madenciliğinden yararlanır.

Kullanıcılar, CRV'yi sonsuz kilitli olan yVault'a yatırır. Karşılığında Backscratcher havuzunun bir payını temsil eden bir token alırlar. Curve üzerinden curve ücreti paylaşımı yoluyla kazanılan gelir, Backscratcher havuzunda dağıtılır ve mevduat sahipleri tarafından haftalık olarak itfa edilir.

Ayrıca, Yearn Finance tarafından kazanılan tüm CRV'nin %10'u Backscratcher'a yatırılır ve sonsuza kadar kilitlenir. Bu nedenle, CRV'yi stake etmek isteyenler doğrudan Curve üzerinden stake yapmaktansa Backscratcher yVault'un aracılığıyla her zaman  daha yüksek bir kar pay alacaklardır. Ayrıca likidite sağlamak için SUSHI ve PICKLE gibi token emisyonları da kazanabilirler.

![](https://i.imgur.com/UfCikwk.png)

Kullanıcılar orijinal CRV'lerini hiçbir zaman geri çekemeyecekler, ancak yveCRV likiditesi üzerindeki teşvikler ve token'in çeşitli gelir kaynaklarından elde ettiği değer nedeniyle, onu başka bir token'le belirli bir fiyat karşılığında takas edebilecekler.

Karşılığında, kilitli CRV'nin güçlendirmeleri üzerindeki kontrol Yearn'e verilir ve çeşitli yVault'larda kullanılır.

## Otomatik compound (bileşik) getirisi

Bileşik getiri, işlem ücretlerinin Ethereum blok zincirine ödenmesini gerektirir. Bu pahalı olabilir ve karda kesinti yapabilir.

yVault'lar işleminizi diğer birçok mevduat sahibiyle gruplandırdığından, kasaları kullanarak getiri elde etmek için kümülatif olarak daha düşük maliyet ve daha yüksek getiri elde edilir. Şu anda, gaz maliyetleri Keep3r ağı tarafından karşılanmaktadır; bu, kullanıcıların hiçbir ücret ödemeden getirileri birleştirdiği anlamına gelir.

## Kaldıraç

Yearn, yVault getirilerini artırmak için kullanılan krediye erişmek için Iron Bank'ı (C.R.E.A.M. Finance) kullanır. Yalnızca beyaz listedeki adresler bu özelliğe sahiptir, yani genellikle bireyler bunu kendi başlarına yapamazlar.

Bazı stratejiler de, yararlanmak için geliştirme deneyimi gerektiren bir back-end hizmeti olan [flash kredileri](https://docs.yearn.finance/resources/defi-glossary#flash-loan) uygular.

## Ortaklıklar

Backscratcher yVault, yalnızca Curve, SushiSwap ve Pickle Finance gibi protokollerle sinerjik ilişkiler sayesinde mümkündür. DeFi genelindeki ilişkilerimiz, yVault mevduat sahiplerine başka yerde alamayacakları avantajlar sağlıyor.

Yearn, sektör olarak verim ve daha fazla DeFi için yeni fırsatlar yaratmak için bahsedilen protokollerle geliştirme konusunda aktif olarak işbirliği yapıyor.
