

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
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE LIGHTNINGPAW -->
## About The LightningPaw

<!-- 
[![Product Name Screen Shot][product-screenshot]](https://example.com)
-->

When it comes to contactless payments, the first thing that comes to mind is NFC cards, which are widely used. 
In principle, however, there are also various other variants of NFC chips, such as stickers, rings or even implants. As long as the NFC chips meet the necessary standards, it doesn't matter what form the chip takes.

Consequently, it should also be possible to authorize Bitcoin lightning payments with a chip implanted in the hand.





<p align="right">(<a href="#readme-top">back to top</a>)</p>




<!-- LNURLw BOLTCARD -->
## LNURLw vs. Boldcard

The easiest way to authorize a Bitcoin Lightning payment with a card is to simply use LNURLw. This simply involves writing a tag to the card with a corresponding URL, which then authorizes the POS terminal to obtain the amount from a specific wallet. However, this URL is static and does not provide any security mechanisms. Under the label Boltcard, LNBits has developed a variant that offers more security. Additional keys are written to a special NFC card and there are additional security mechanisms. Creating such cards is relatively easy. Especially if you use the app [https://play.google.com/store/apps/details?id=com.lightningnfcapp] (Boltcard NFC Programmer). This mechanism requires NFC cards of type NTAG424DNA or NTAG424DNATT. Detailed instructions can be found on the github account of  [https://github.com/lnbits/lnbits/tree/main/lnbits/extensions/boltcards](lnbits).

Unfortunately, there are no implants of this type on the market at the moment. There are implants with additional security and encryption options, but they are not compatible.

Thus, we have to keep it simple and use the not really secure static LNURLw. It is not a problem since we can limit the amount per transaction and also how often a payment can be authorized. 


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
### Usage
Setup an LNBits Wallet and activate the LNURL-withdraw extension.
Do the configuration in the config.ini file. Maybe you also like to change the desing of the voucher. Just define an other background image.

 ```sh
   python main.py
   ```
<p align="right">(<a href="#readme-top">back to top</a>)</p>







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
