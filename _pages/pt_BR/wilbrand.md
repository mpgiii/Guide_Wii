---
title: "Wilbrand"
---

Se você precisa de ajuda sobre qualquer coisa deste tutorial, por favor entre [no servidor do Discord RiiConnect24](https://discord.gg/rc24) (recomendado) ou [mande um e-mail para support@riiconnect24.net (em inglês)](mailto:support@riiconnect24.net).
{: .notice--info}

![Wilbrand](/images/wilbrand/icon.png)

Wilbrand, like LetterBomb, is an exploit for the Wii that is triggered using the Wii Message Board.

Unlike LetterBomb, Wilbrand supports Wii menu versions down to 3.0.
{: .notice--info}

#### Você precisará de

- A PC running Windows, MacOS or Linux
- Um cartão SD formatado para FAT32/MS-DOS
- A Wii on at least version 3.0
- [Wilbrand](https://static.wiidatabase.de/Wilbrand.zip)
- [HackMii Installer v1.2](https://bootmii.org/download/)

#### Instruções

1.  On your Wii, go to `Wii Settings`, and make note of the version at the top right. Proceed to `Internet` -> `Console Information` and also make note of your MAC address.
1.  Extract the Wilbrand zip to a folder on your PC, preferably on your desktop.
1.  Insert your SD card into your PC.
1.  Open a terminal inside the folder Wilbrand was extracted to.
1.  Using your Wii's version and MAC address, run the following command:

- Windows: `.\Wilbrand.exe AA-BB-CC-DD-EE-FF MM/DD/YYYY VERSION X:`

  - `X:` is the drive letter of your SD card. ![running Wilbrand on Windows](/images/wilbrand/windows.png)

- Linux/MacOS: `./Wilbrand AA-BB-CC-DD-EE-FF MM/DD/YYYY VERSION /media/mount_dir`
  - If you have not opened your terminal directly in the folder Wilbrand was extracted to, use `cd` to enter it first, eg. `cd ~/Desktop/Wilbrand`
  - `/media/mount_dir` is the folder your SD card is mounted in. This may vary depending on your Linux distro. ![running Wilbrand on Linux](/images/wilbrand/linux.png)

1.  Extract the HackMii Installer v1.2 to a folder on your PC.
    - You may also simply open the zip file in your archive manager.
1.  Locate the `boot.elf` file, and put it on the root of your SD card.
1.  Pegue seu cartão SD e insira-o no seu Wii.
    - O cartão SD deve ser inserido no slot de cartão SD localizado na frente do Wii. O uso de um adaptador USB conectado à porta USB do Wii não funcionará.
1.  No seu Wii, retorne ao Menu do Wii e então abra o Wii Message Board.
1.  Load the green letter with the Bob-omb icon.
    - Certifique-se que a data em seu Wii está correta, caso contrário você não poderá encontrar a carta.
    - The mail may have appeared on the previous or next day.
    - If you don't see the green letter, check if any errors appear in the SD card sections in `Data Management`. If any do, there may be an issue with the SD card format or the Wii's SD card reader. ![Wilbrand in its natural habitat](/images/wilbrand/msgboard.png)

[Continue para a Instalação do Homebrew Channel e do BootMii](hbc)
{: .notice--info}