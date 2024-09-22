---
title: "Credits"
---

{% include toc title="Table of Contents" %}

## BlueBomb Micro

{% capture technical_info %}
<summary><em>Technical Details (optional)</em></summary>
BlueBomb Micro is a port of Fullmetal5's BlueBomb exploit for the Rasperry Pi Pico W or ESP32, thus bypassing the need for a Linux system. It takes advantage of a flaw in the Wii and Wii mini's Bluetooth libraries. This port was made possible by [GaryOderNichts](https://github.com/GaryOderNichts)

This exploit also enables recovery from certain bricks, such as banner bricks and (some) theme bricks.

{% endcapture %}
<details>{{ technical_info | markdownify }}</details>
{: .notice--info}

Il est **vivement** déconseillé d'utiliser **n'importe quel** guide vidéo pour hacker votre console Wii mini, puisqu'il y a une très grande chance de la **bricker**.
{: .notice--warning}

Si vous avez besoin d'aide pour tout ce qui concerne ce tutoriel, veuillez rejoindre [le serveur Discord Wii mini Hacking](https://discord.gg/6ryxnkS) (recommandé)
{: .notice--info}

For the original Wii, we do not recommend using BlueBomb if you intend to install the Homebrew Channel and BootMii, as there are more convenient exploits available. Toutefois, des exceptions existent dans des circonstances telles que la récupération de bricks.
{: .notice--info}

Assurez-vous que la console est proche de l'ordinateur qui exécute l'exploit, idéalement à moins de 1 mètre.
{: .notice--info}

### Prérequis
* A Rasperry Pi Pico W or an ESP32 with BR/EDR (Classic) support.
* Une clé USB formatée en FAT32.
* [The HackMii Installer](https://bootmii.org/download/)

A normal Rasperry Pi Pico will not work. It MUST to be the wireless model. Additionally, an ESP32 with a BLE only controller will not work.
{: .notice--info}

### Instructions

1. Extract it and place the `boot.elf` file in your flash drive.
    + (Si vous essayez de réparer un brick, vous devrez également copier l'application homebrew que vous souhaitez utiliser dans /apps/)
    + - (Even for a Wii mini, bootmini.elf will **not** work, its purpose is entirely different and unrelated. Utilisez boot.elf dans tous les cas).
1. Réinsérez votre clé USB dans votre console.
    + Pour une Wii mini, le port USB est à l'arrière.
    + For a normal Wii, use the bottom port. (or the right port if it's upright).
1. Allumez votre console.
1. Allez sur `Paramètres Wii`.
1. Prenez note dans le coin supérieur droit de la lettre à côté de la version du système.
    + Cette lettre est la région du menu système, que vous devrez connaître pour les étapes qui en ont besoin.

    ![](/images/wii/SystemMenuVersion.png)

1. Éteignez votre console.

#### Rasperry Pi Pico W

1. Download [The latest Pre-Compiled Binaries](https://github.com/GaryOderNichts/bluebomb_micro/releases) from the releases page, and extract it to your PC.
1. Plug in your Pico W to your PC while holding down the `BOOTSEL` button. Your Pico should now show up as a drive on your PC.
1. Unzip the downloaded file and copy the file which matches your Wii or Wii mini to the drive. For example, if you have a European Wii running version 4.3, you would copy bluebomb_WII_SM4_3E.uf2, or if you have a European Wii Mini, you would copy bluebomb_MINI_SM_PAL.uf2, etc...
1. The drive should disconnect and your Pico is ready. You may unplug the device from your PC.

#### ESP32

1. Set up the latest [ESP IDF](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/index.html).
1. Build the binary [from source](https://github.com/GaryOderNichts/bluebomb_micro/tree/main/ports/esp32#building-from-source).
1. [Flash the binary](https://github.com/GaryOderNichts/bluebomb_micro/tree/main/ports/esp32#flashing) to your ESP32.
1. Your device is now ready. You may unplug the device from your PC.

### Performing the Exploit

1. Plug your flashed device back into your PC.
1. Éteignez votre console.
    + Turn on your console and **do not** connect any Wii Remotes.
1. Press the Sync button repeatedly until the bluebomb screen shows up.
    + Cela peut demander de nombreuses tentatives.
1. Si l'exploit a réussi, votre console aura chargé l'installeur HackMii.

If using a Wii, proceed to installing the Homebrew Channel and BootMii<br>
{: .notice--info}

If using a Wii mini, proceed to installing the Homebrew Channel
{: .notice--info}

## BlueBomb Classic

Bien que ce soit le seul exploit qui fonctionne pour la Wii mini, BlueBom peut aussi fonctionner sur la Wii originale. {% capture technical_info %}
<summary><em>Technical Details (optional)</em></summary>
BlueBomb is an exploit that takes advantage of a flaw in the Wii and Wii mini's Bluetooth libraries.

This exploit also enables recovery from certain bricks, such as banner bricks and (some) theme bricks.

{% endcapture %}
<details>{{ technical_info | markdownify }}</details>
{: .notice--info}

Il est **vivement** déconseillé d'utiliser **n'importe quel** guide vidéo pour hacker votre console Wii mini, puisqu'il y a une très grande chance de la **bricker**.
{: .notice--warning}

Si vous avez besoin d'aide pour tout ce qui concerne ce tutoriel, veuillez rejoindre [le serveur Discord Wii mini Hacking](https://discord.gg/6ryxnkS) (recommandé)
{: .notice--info}

For the original Wii, we do not recommend using BlueBomb if you intend to install the Homebrew Channel and BootMii, as there are more convenient exploits available. Toutefois, des exceptions existent dans des circonstances telles que la récupération de bricks.
{: .notice--info}

Assurez-vous que la console est proche de l'ordinateur qui exécute l'exploit, idéalement à moins de 1 mètre.
{: .notice--info}

### Prérequis

* Une machine Linux
    * Une machine virtuelle peut fonctionner, mais elle n'est pas recommandée dû à la complexité à faire fonctionner le Bluetooth. Si possiblez, utilisez un LiveUSB comme décrit ci-dessous.
    * Si vous avez un Raspberry Pi, vous pouvez l'utiliser vu qu'il est très probable que Linux soit déjà installé.
    * Le sous-système Linux pour Windows ou un Chromebook en mode Linux ne *marcheront pas* vu qu'ils n'ont pas d'accès direct à l'adaptateur Bluetooth ou aux ports USB.
    * Si vous n'avez pas Linux, [Ubuntu](https://ubuntu.com/download/desktop) est l'option la plus conviviale et peut être exécutée sur des ordinateurs fonctionnant sous Windows ou Mac.
        * Les appareils 32 bits nécessiteront [Ubuntu 16.04](http://releases.ubuntu.com/16.04/).
        * Pour les appareils 64 bits, il est recommandé d'utiliser l'édition LTS en raison de sa stabilité, mais la dernière version fonctionne également.
    * Vous pouvez [flasher un environnement Linux vers une clé USB](https://ubuntu.com/tutorials/tutorial-create-a-usb-stick-on-windows#1-overview) au lieu de l'installer sur votre ordinateur.
* Un adaptateur Bluetooth.
    * Un adaptateur Bluetooth interne fonctionne.
    * Si vous n'en avez pas, assurez-vous d'en prendre un compatible avec Linux.
* Une clé USB formatée en FAT32.
    * Elle ne peut pas être la même que celle utilisée pour votre machine Linux.
* [HackMii Installer v1.2](https://bootmii.org/download/)

### Instructions

1. Extract it and place the `boot.elf` file in your flash drive.
    + (Si vous essayez de réparer un brick, vous devrez également copier l'application homebrew que vous souhaitez utiliser dans /apps/)
    + - (Even for a Wii mini, bootmini.elf will **not** work, its purpose is entirely different and unrelated. Utilisez boot.elf dans tous les cas).
1. Réinsérez votre clé USB dans votre console.
    + Pour une Wii mini, le port USB est à l'arrière.
    + For a normal Wii, use the bottom port. (or the right port if it's upright).
1. Allumez votre console.
1. Allez sur `Paramètres Wii`.
1. Prenez note dans le coin supérieur droit de la lettre à côté de la version du système.
    + Cette lettre est la région du menu système, que vous devrez connaître pour les étapes qui en ont besoin.

    ![](/images/wii/SystemMenuVersion.png)

1. Éteignez votre console.
1. Démarrez votre distribution Linux et assurez-vous que vous êtes connecté à Internet.
1. Ouvrez le Terminal
1. Exécutez les commandes suivantes :

    ```bash
    wget https://wii.hacks.guide/assets/files/bluebomb-helper.sh
    chmod +x bluebomb-helper.sh
    ./bluebomb-helper.sh
    ```

1. L'assistant téléchargera ensuite les fichiers requis et vous demandera des informations sur votre console.
    + Si vous avez sélectionné une Wii Mini, il vous sera demandé de fournir votre région. Ceci est déterminé par la dernière lettre de la version du menu Wii (`U` pour **USA** et `E` pour les modèles **PAL**).
    + Si vous avez sélectionné une Wii, il vous sera demandé de fournir la version de votre menu Wii (Ce que vous avez déterminé à l'étape 4)
1. Allumez votre console.
    + Turn on your console and **do not** connect any Wii Remotes.
1. Appuyez sur le bouton **Sync** plusieurs fois jusqu'à que le terminal affiche `got connection handle`.
    + Cela peut demander de nombreuses tentatives.
1. Si l'exploit a réussi, votre console aura chargé l'installeur HackMii.
    + You can now shut down your Linux computer if you are not planning to use it later.

If using a Wii, proceed to installing the Homebrew Channel and BootMii<br>
{: .notice--info}

If using a Wii mini, proceed to installing the Homebrew Channel
{: .notice--info}