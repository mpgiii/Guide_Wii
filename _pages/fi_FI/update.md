---
title: "Updating Wii Menu to v4.3"
---

{% include toc title="Sisällysluettelo" %}

Jos tarvitset apua missä tahansa tähän oppaaseen liittyvässä, liity [RiiConnect24:n Discord-palvelimelle](https://discord.gg/rc24) (suositeltavaa) tai [ lähetä meille sähköpostia osoitteeseen support@riiconnect24.net](mailto:support@riiconnect24.net).
{: .notice--info}

This tutorial will explain how to update your Wii Menu to version 4.3, as you can no longer use the updater built into the Wii Menu since the servers are no longer up.

#### Mitä tarvitset
* SD-kortti tai USB-asema
* A computer with Windows on it
* [IOS58 Installer](https://oscwii.org/library/app/ios58-installer)
* [NUS Downloader](https://github.com/WiiDatabase/nusdownloader/releases/latest)
* [Wii Mod Lite](https://oscwii.org/library/app/WiiModLite)

If you don't have a Windows computer, please join [the RiiConnect24 Discord server](https://discord.gg/rc24) (recommended) or [e-mail us at support@riiconnect24.net](mailto:support@riiconnect24.net).
{: .notice--info}

#### Ohjeet

##### Osa I - Lataaminen

Your Wii must be modded in order to perform this. If it isn't, then it's best to follow [the guide](get-started) first before doing this.
{: .notice--info}

To protect against bricks, [make sure you install Priiloader](priiloader). Also, install [BootMii](bootmii) (as Boot2 if you have an early Wii, otherwise IOS). Installing brick protection along with following the guide correctly should keep you safe from bricks. ÄLÄ JATKA ENNEN KUIN OLET ASENTANUT PRIILOADERIN JA BOOTMIIN!
{: .notice--danger}

1. Extract the .zip file for NUS Downloader vWii and open the application.
2. Go to `Database...` > `System` > `0000000100000002 - System Menu` and select the version corresponding to your region as shown in the table below.
3. Make sure `Pack WAD` is checked.
4. Press `Start NUS Download!`.
5. Open the `titles` -> `0000000100000002` -> (Wii Menu version) and copy the .wad file to a folder called `wad` on your SD Card or USB drive.
6. (If you have [RiiConnect24](riiconnect24), you can skip this step) Repeat steps 2-5 with `IOS` -> `0000000100000050 - IOS80` -> `Latest Version`.

| Region | Wii Menu version |
| ------ | ---------------- |
| Japan  | v512 (4.3J)      |
| USA    | v513 (4.3U)      |
| Europe | v514 (4.3E)      |
| Korea  | v518 (4.3K)      |

##### Osa II - Asentaminen

You use the +Control Pad to use this tool.
{: .notice--info}

1. Put your SD card or USB drive in your Wii.
2. Käynnistä Homebrew Channel Wii:lläsi.
3. Launch Wii Mod Lite.
4. Käyttämällä +Control Pad:ia Wii Remotella, navigoi kohtaan `WAD Manager`, ja siirry sitten `wad` -kansioon.
5. Press A to install the IOS80. [`Make sure the installation is successful, otherwise abort.`]
6. Press A to install the Wii Menu WAD.
7. Kun ne on asennettu onnistuneesti, paina HOME-painiketta poistuaksesi Homebrew Channeliin.
8. Launch IOS58 Installer.
9. Follow the instructions to install IOS58.

[Continue to Priiloader Installation](priiloader)<br> Priiloader adds a level of brick protection, and we recommend it.
{: .notice--info}