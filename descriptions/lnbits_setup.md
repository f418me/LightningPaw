# Setup LNbits LNURLw

LNBits is an application that sits on top of the Lightning network and implements various protocols such as LNURLw. There are also other possibilities but in our case we’ll be using LNBits.
LNBits can be run on your own Lightning Node or you can use a hosted wallet.
In our demo example, we use the Legend solution hosted by [LNBits](https://legend.lnbits.com)

## Setup a new Wallet

 ![](https://raw.githubusercontent.com/f418me/LightningPaw/master/images/lnbits_account.png)

## Activate LNURLw Extension.
 
Send some sats to the wallet.
Generate a new LNURLw link and customize it.


 ![](https://raw.githubusercontent.com/f418me/LightningPaw/master/images/lnbits_lnurlw.png)


Now we get an URL which lock like this:


 ```
   LNURL1DP68GURN8GHJ7MR9ZAJKUEPWD4HWY6T5WVHXXMMD9AMWJARGV3EXZAE0V5CXJTMGXYHKCMN2WFGZ7DJ9VU68X328VF3K8J6TXS64QNN02PA9J4RE0VLVCR
```
With this URL or with the representing QR Code we are able to withdraw from the LBits Service. We just need an LNURLw compatible Wallet. Which wallets are supporting which LNURL protocoll can be found [here](https://github.com/lnurl/luds).