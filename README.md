

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/f418me/LightningPaw">
    <img src="https://github.com/f418me/LightningPaw/images/bild_title.jpg" alt="Logo" width="500" height="300">
  </a>

  <h3 align="center">Lightning Paw, pay with your hand</h3>

  <p align="center">
    Lightning payments with an implant.
    <br />
    <br />
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-lightningpaw">About the LightningPaw</a></li>
    <li><a href="#LNURLw-Boldcard">LNURLw vs. Boldcard</a></li>
    <li><a href="#LNURL">LNURL</a></li>
    <li><a href="#disclaimer">Disclaimer</a></li>
    <li><a href="#implants">Implants</a></li>
    <li><a href="#setup-nfc-implant">Setup NFC Implant</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE LIGHTNINGPAW -->
## About The LightningPaw

<!-- 
[![Product Name Screen Shot][product-screenshot]](https://example.com)
-->

When it comes to contactless payments, the first thing that comes to mind is NFC cards, which are widely used. In principle, however, there are also various other variants of NFC chips, such as stickers, rings or even implants. As long as the NFC chips meet the necessary standards, it doesn't matter what form the chip takes.

Consequently, it should also be possible to authorize Bitcoin lightning payments with a chip implanted in the hand.




<p align="right">(<a href="#readme-top">back to top</a>)</p>




<!-- LNURLw BOLTCARD -->
## LNURLw vs. Boldcard

The easiest way to authorize a Bitcoin Lightning payment with a card is to simply use LNURLw. This involves writing a tag to the card with a corresponding URL, which then authorizes the POS terminal to obtain the amount from a specific wallet. However, this URL is static and does not provide any security mechanisms. Under the label Boltcard, LNBits has developed a variant that offers more security. Additional keys are written to a special NFC card and there are additional security mechanisms. Creating such cards is relatively easy. Especially if you use the app [Boltcard NFC Programmer](https://play.google.com/store/apps/details?id=com.lightningnfcapp). This mechanism requires NFC cards of type NTAG424DNA or NTAG424DNATT. Detailed instructions can be found on the github account of [lnbits](https://github.com/lnbits/lnbits/tree/main/lnbits/extensions/boltcards).

Unfortunately, there are no implants of this type on the market at the moment. There are implants with additional security and encryption options, but they are not compatible.

Thus, we have to keep it simple and use the not really secure static LNURLw. It is not a problem since we can limit the amount per transaction and also how often a payment can be authorized. 


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- DISCLAIMER -->
## Disclaimer

Static LNURLw links are not secure and not suitable for large amounts. Firstly, the chip can be read. Secondly, the static URL is communicated to the POS device during a payment. So the link could then be used to make further withdrawals.

Use this only if you either know what you are doing or you are a reckless lightning honey badger. Only you are responsible for all your sats, wallets, cards and other devices. Always backup! 

Regarding implants, it does not tolerate fun. Implant placement, if done incorrectly, can lead to serious problems. Always follow the instructions of the respective companies and have the procedure done only by professionals such as piercers or doctors.



<!-- IMPLANTS -->
## Implants

There are various implants. But pay attention, the simple RFID models that are implanted into cats do not work.  They just have an ID and it's not possible to write a custom tag on it. It must be possible to create an own tag on the NFC implant.

We have chosen the following model:

ISO 14443-SA NXP - NTAG216 available at [digiwell.com](https://digiwell.com/).

Likewise would work for example (simply if such implants would exist):

ISO 14443-3A NXP - Mifare Classic
ISO 14443-3A NXP - NTAG215

Often these are grouped under the label X2 Series. 

In general, it can be said that you need an Android phone to write. Reading works partially with the iPhone, for example with ISO 14443-3A NXP - Mifare Classic. Depending on the application, however, not everything is working correctly on the iPhone. Currently, Apple still restricts the NFC protocol in certain aspects. For example, the implant we used does not work with the iPhone. 



<!-- LNURL -->
## LNURL

LNURL is a stack of simple protocols for coordinating information needed to make payments over the Lightning Network using HTTP. A full documentation about LNURL can be found here. 
The LNURL protocol contains 3 core features such as an authentication scheme, where a public key can be used to log in to a service, an invoice request scheme where a wallet can ping a server through a static QR code (URL) and retrieve an invoice, and a withdraw request scheme where a wallet can ping the server and request that the server pays an invoice provided by the wallet. 
The LNURLw withdrawal works by giving the wallet an URL to ping the service and in response, receiving a description which contains a URL to send an invoice to, a random string (or deterministic to tie to an account or user) and a minimum amount aswell as a maximum amount that can be withdrawn. After filling in the appropriate value, the wallet returns the invoice to the server;if it is valid and within the amount parameters, the service on the server pays the invoice.

This static LNURLw URL can be used to do payments with NFC chips.


## LNBits
LNBits is an application that sits on top of the Lightning network and implements various protocols such as LNURLw. There are also other possibilities but in our case we’ll be using LNBits. Details can be found [here](https://github.com/f418me/LightningPaw/blob/master/descriptions/lnbits_setup.md).


<!-- SETUP NFC IMPLANT -->
## Setup NFC implant

We need a device to write a NFC Tag to the implant. The simplest solution is just to use an Android smartphone and the App NFC Tools.

 We need to add a tag of the Typ "Custom URL / URI"

The record must be the LNURlw URL string with the prefix "lightning:"


 ```
   lightning:LNURL1DP68GURN8GHJ7MR9ZAJKUEPWD4HWY6T5WVHXXMMD9AMWJARGV3EXZAE0V5CXJTMGXYHKCMN2WFGZ7DJ9VU68X328VF3K8J6TXS64QNN02PA9J4RE0VLVCR
   ```

After that, we just write this record to the implant and we are ready to pay. Details can be found [here](https://github.com/f418me/LightningPaw/blob/master/descriptions/implant_setup.md).






<!-- LICENSE -->
## License
This work is licensed under the Creative Commons Attribution-ShareAlike 4.0
International License. To view a copy of this license, visit
[http://creativecommons.org/licenses/by-sa/4.0/](http://creativecommons.org/licenses/by-sa/4.0/).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

f418.me - [f418_me](https://twitter.com/f418_me) - info@f418.me


<p align="right">(<a href="#readme-top">back to top</a>)</p>




<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/company/f418-me/
[product-screenshot]: images/screenshot.png
