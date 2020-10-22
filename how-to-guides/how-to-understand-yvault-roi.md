# Comprendre le ROI du yVault

### ROI

Êtes-vous un utilisateur avancé qui essaie de comprendre comment le retour sur investissement est calculé? Passer directement à "Pourquoi nous ne pouvons pas utiliser de formules d'intérêts composés ou linéaires pour estimer les rendements de yVaults"

Are you an advanced user trying to understand how ROI is calculated? Skip directly to "[_Why we can't use compound or linear interest formulas to estimate yVaults returns_](https://docs.yearn.finance/how-to-guides/how-to-understand-yvault-roi#why-cant-we-use-compound-or-linear-interest-formulas-to-estimate-yvaults-returns)"

Si vous êtes un débutant en DeFi ou un nouvel utilisateur de Yearn, continuez à lire.

#### Définition du ROI :

> Le retour sur investissement \(ROI\) est un rapport entre le bénéfice net \(sur une période\) et le coût de l'investissement \(résultant d'un investissement de certaines ressources à un moment donné\). Un retour sur investissement élevé signifie que les gains de l'investissement se comparent favorablement à son coût. En tant que mesure de la performance, le retour sur investissement est utilisé pour évaluer l'efficacité d'un investissement ou pour comparer l'efficacité de plusieurs investissements différents. \[1\] En termes économiques, c'est une façon de relier les bénéfices aux capitaux investis. Source: [Wikipédia](https://en.wikipedia.org/wiki/Return_on_investment)

* ROI is a key performance indicator \(KPI\) available in all Yearn Vaults \(yVaults\) located here: [https://yearn.finance/vaults](https://yearn.finance/vaults).
* ROI is useful when comparing and assessing vault performance.
* ROI presented in Yearn is a **yearly ROI**. You deposit X and 1 year later you receive X + \(X \* ROI\).
* The ROI presented is a _current estimation_ based on data since the yVault's inception. If performance remains constant, after 1 year you will receive the displayed ROI. Rates are unstable currently, and fluctuate based on market/strategy.

yVaults a différentes [stratégies](https://docs.yearn.finance/faq#vault-stratégies) de rendement \(yield farming\), qui déterminent la façon dont les actifs sont déplacés entre les pools de liquidités. Les stratégies sont créées par le `Controller` qui gère le yVault.

De nouvelles stratégies sont également votées par la communauté à travers des [propositions de gouvernance](https://gov.yearn.finance/). Une nouvelle stratégie crée un nouveau challenge en termes de calcul du ROI.

* Individuals interested in participating in a yVault should monitor the ROI presented in the vault dashboard after a strategy change. The rate presented reflects the most recent ROI.
* An individual participating before a strategy change might be interested in comparing ROI before and ROI after. Historic ROI, e.g. since yVault creation, can also help users understand performance and inform future decisions.

## Calcul du ROI 

Même si le yVaults a un effet composé par nature, cet intérêt composé n'est pas fixe comme dans un compte d'épargne CeFi. Par conséquent, le concept [d'APY](https://www.investopedia.com/terms/a/apy.asp) et [d'APR](https://www.investopedia.com/terms/a/apr.asp) ne s'applique pas directement aux yVaults. Ils sont utilisés par la communauté, mais leur interprétation doit être prise des pincettes.

### Pourquoi nous ne pouvons pas utiliser de formules d'intérêts composés ou linéaires pour estimer les rendements de yVaults ?

* Cela montre l'estimation d'un actif auquel sont appliqués des intérêts / intérêts composés:

![](https://i.imgur.com/OZKqesB.png)

* Il s'agit de la performance réelle et mesurée d'un actif dans le vault yUSD:

![](https://i.imgur.com/NpogiO9.png)

### Pourquoi cela arrive-t-il ?

A bank's interest rate is constant: either linear or compounding. The interest rate is multiplied by the asset value each period.

yVaults work differently:

After depositing into a yVault, the user receives 'wrapped' tokens. These tokens start with a 'y' prefix and the depositor receives fewer tokens than were deposited \(why is explained below\).

Starting from its inception, the vault's input and output are governed by the following equation:

$$F = I * P$$

Where $F$ is the amount of the tokens in the vault, $I$ is the amount of 'wrapped' tokens held by users and $P$ is the 'price' of those wrapped tokens.

At the start, $$P = 1$$

Thus $$I = F$$, amount of tokens inside the vault is equal to amount of wrapped tokens.

**Almost all strategies are identical**: invest deposited tokens, accumulate additional tokens which can be withdrawn in the future.

By keeping track of the number of wrapped tokens, and the amount of tokens inside the vault \(which increase the longer they are held in the vault\) the price can be calculated as follows:

$$(vault tokens) / (wrapped tokens) = P$$

Since the amount of wrapped tokens is constant but the amount of vault tokens increases, the price will increase.

The balance and thus price are therefore constantly increasing.

Therefore, the only thing we can do is:

* Try to use data from two different points in time
* Assume growth is linear \(because simply there is no other information we have\)
* Construct a line using both points which we then extrapolate
* Calculate price at future data to display ROI.

However, as shown below this is dependent on where we take those points.

### ROI extrapolation applied to the yUSD Vault chart

Below are examples to show different results possible by applying linear extrapolation to two points of the price chart for the yUSD yVault.

First of all, why and how is this done?

Vault input/output formula:

$$F = I * P$$

Now, we want to calculate the increment of $F$ which would be our return.

Since $I$ is constant, and only $P$ changes, if we know $P$ at a future date, we can calulate our return.

In order to get the formula for a line having two points we have to do some math:

Formula for a line: $$y = m*x + c$$

where $y$ is the price, $x$ is the block height and $m$, $c$ are what we are looking for.

First, let's get $c$.

When $x = 0$ \(so at inception of the yVault\), we know that the price is 1, hence: $y = m\*0+c$ \(x = 0\) $y = c$ $y = 1$ \(price is 1 when x = 0\) $c = 1$

Now m \(here we have to apply derivatives\):

Using the product formula and the constants formula:

$y'\(x\) = m$

Approximating the derivative of a linear function can be done by:

$y'\(x\) = \(y2-y1\)/\(x2-x1\) = m$

$y2$ being the price at block $x2$ and $y1$ the price at block $x1$.

Finally we have the complete formula and can estimate the price at any date in the future.

However, since $y\(x\)$ is **not** linear, we get different lines for different points \(shown below\).

As a result, our estimation for price in future and the return varies greatly depending on which points we choose.

Here we take two points of the performance chart for the yUSD vault \(numbered colored points\) and apply the above. Notice that the different lines are relatively good indications for the short term, but when we try to use them to predict long term they're totally inaccurate!

![](https://i.imgur.com/g2I40pQ.png)

### Example

Jane has 100 yCRV tokens and decides to invest them in the yUSD yVault.

At that time the price $P$ is 1.045, the total number of vault tokens is 10,450 and of wrapped tokens 10,000. $$10450 / 10000 = 1.045$$

Now her yCRV tokens get adjusted according to the formula above which is why she sees her now wrapped tokens \(yUSD\) reduce in quantity and the tokens in the vault \(yCRV\) are equal to the amount she invested.

So, how many wrapped tokens will she receive?

$$I = F/P = 100/1.045 = 95.7 yUSD$$

This action, did **not** change the price because she supplied to the number of wrapped tokens and vault tokens each exactly according to the ratio of the current price. This is quite important since it means that deposits and withdrawals will not have any effect on the price of the wrapped token.

Fast forward a few days, the strategy uses Jane's funds to yield farm and uses the profits to purchase more tokens held inside the vault, increasing the balance to 10,500. For simplicity's sake, assume there were no other deposits. The wrapped tokens are still 10,000 and thus: $$P = 10500/10000 = 1.05$$

When Jane now looks at her balance of wrapped tokens, she will see that they have incremented to approx.:

$$F = I * P = 95.7 * 1.05 = 100.5$$

At this point, she could withdraw and receive her initial yCRV deposit and an additional amount of yCRV tokens, giving her a return of 0.5% on her initial investment \(ignoring the 0.5% withdrawal fee\).

### Conclusions

1. The short-term ROI data is a suitable estimation for the short-term \(i.e. if we compare the % from the last two days, it's likely that the following two days are going go be similar\).
2. Short-term ROI data is _**absolutely not accurate**_ when extrapolated in the long-term.
3. Long-term data \(say today and [inception of vault](https://docs.yearn.finance/faq#lists-of-smart-contracts)\) is a good overall estimation of the vaults performance and should be used when comparing different investment opportunities.

In other words, if your goal is to approximate returns in the short-term, you should use datasets that are recent \(daily/weekly\).

If you would like to make a crude estimation on how returns may look like in a year or longer, the longest possible historic timeframe should be taken.

### Other references

The community has been actively creating tools and guides on this topic.

* [https://github.com/thegismar/yearn\_roi/blob/master/yearn\_vaults\_ROI\_calc.ipynb](https://github.com/thegismar/yearn_roi/blob/master/yearn_vaults_ROI_calc.ipynb) provides a mathemathical explanation on how ROI is calculated with some caveats. \(This repository is no longer being maintained\).
* [Statistics FAQ](https://docs.yearn.finance/faq#statistics)
* [yVault ROI performance over time graph](https://py-earn.herokuapp.com/graph)

