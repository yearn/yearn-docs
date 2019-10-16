# Iframe Integration

Uniswap can be used within other sites as an Iframe. This Iframe shows an exact version of the uniswap.exchange site and can have custom prefilled settings. 

#### Live Example

An example of an Iframe integration can be found on the FOAM site https://map.foam.space/#/at/?lng=-74.0045300&lat=40.6771800&zoom=5.00

To see the Iframe click the dropdown in the top right and click "get foam". 

![Foam Iframe Example](.gitbook/assets/foamiframe.png)

You can customize the page, selected custom tokens and more using URL query parameters. See https://docs.uniswap.io/frontend-integration/linking for more. 

#### Add To Your Site

To include a Uniswap iframe within your site just add an iframe element within your website code and link to the Uniswap exchange. 

Linking to a ETH <-> DAI swap page would look something like

```            
<iframe
  url="https://uniswap.exchange/swap?outputCurrency=0x89d24a6b4ccb1b6faa2625fe562bdd9a23260359"
  height="600px"
  width="600px"
  id="myId"
  display="initial"
  position="relative"
/>```
