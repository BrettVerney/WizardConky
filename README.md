# WizardConky

One of my favourite Conky desktops. I run this on Manjaro but should work with any Linux desktop providing it supports the Conky package.

## Install

Depending on what OS you are running...

**RedHat based systems:**<br>
```yum install conky```<br>

**Debian based systems:**<br>
```apt-get install conky-all```<br>

**Arch based systems:**<br>
```pacman -Sy --noconfirm conky```<br>

...you can figure out the rest.

## Setup

**Create the Conky config directory:**<br>
```mkdir -p ~/.config/conky```<br>

**Create an emppty Conky config file:**<br>
```touch ~/.config/conky/conky.conkyrc```<br>

 and paste the contents from my **conky.conkyrc** file.

**Create a a script to run Conky at boot:**<br>
```echo -e '#!/bin/bash \n sleep 10 && conky -d -c ~/.config/conky/conky.conkyrc &' >> conky_start.sh```<br>

It's up to you to figure out how to trigger the script at boot. This is dependent on your OS and/or desktop environment.


## Screenshots

![WizardConky Example 1](https://github.com/BrettVerney/WizardConky/blob/main/screenshot1.jpg)<br>
![WizardConky Example 2](https://github.com/BrettVerney/WizardConky/blob/main/screenshot2.jpg)

## Tips

- Upload your own icon to **~/.config/conky/icon.png**
- Play with the **--WINDOW & BORDERS SETTINGS** to make it work with your graphics card, and screen resolution
- Update the font size if it is too small or large on your system
- Add your own storage volumes and mount points under the **Storage** section. List them running ```df``` at the terminal.
- Use your own Wi-Fi and Wired NIC names. Replace all instances of ***wlp58s0*** (Wi-Fi) and ***enp0s20f0u1*** (Wired). Find them by running ```ip link show``` athe the terminal.
- Check out the full list of [Conky Objects](http://conky.sourceforge.net/variables.html)
- Use the ```execi <frequency_in_sec> nmcli <shell_command>``` to output native linux commands to the desktop.
- Have fun!
