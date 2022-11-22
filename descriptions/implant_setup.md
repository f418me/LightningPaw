# Setup implant

Descriptions on how to inject the implant can be found directly on [digiwell.com](https://digiwell.com/bodyhacking-installation).

So let's assume we have a working implant. 

We need a device to write a NFC Tag to the implant. The simplest solution is just to use an Android smartphone and the App [NFC Tools](https://play.google.com/store/apps/details?id=com.wakdev.wdnfc).


## Reading NFC implant
First we just check if we can read the implant.

<img src="https://raw.githubusercontent.com/f418me/LightningPaw/master/images/phone_read_implant.png" alt="drawing" width="200"/>

<br>

## Setup and write a new record

 We need to add a new record  of the Typ "Custom URL / URI"
phone_add_record

he record must be the LNURlw URL string with the prefix "lightning:"

<img src="https://raw.githubusercontent.com/f418me/LightningPaw/master/images/phone_lnurlw.png" alt="drawing" width="200"/>

<img src="https://raw.githubusercontent.com/f418me/LightningPaw/master/images/phone_tag.png" alt="drawing" width="200"/>

<br>
Now we can write down the record

<img src="https://raw.githubusercontent.com/f418me/LightningPaw/master/images/phone_write.png" alt="drawing" width="200"/>

<br>

## Verify record on implant
After writing the record we can just read the implant again an check if we see the record.

<img src="https://raw.githubusercontent.com/f418me/LightningPaw/master/images/phone_finished.png" alt="drawing" width="200"/>