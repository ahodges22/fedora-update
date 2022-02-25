# fedora-update
Update indicator for Fedora Linux and [Gnome](https://www.gnome.org/) Shell

![Screenshot](https://raw.githubusercontent.com/pepe386/fedora-update/master/indicator.png)

## Features
- Optional update count display on panel
- Optional notification on new updates (defaults to off)
- Launcher for your favorite update command

## Manual install
To install, simply download and execute "make install"

## One-click install
It's on [Gnome Shell Extensions](https://extensions.gnome.org/extension/4415/fedora-linux-updates-indicator/)

## Without Password Prompt

The authorization is done by pkexec. Therefore if you would like to be able to start dnf services without getting prompted for a password, you will have to configure a polkit policy. The policy file 
[org.freedesktop.policykit.pkexec.fedora-update.policy](https://github.com/pepe386/fedora-update/blob/master/org.freedesktop.policykit.pkexec.fedora-update.policy) would allow the execution of `dnf [check-update|list updates]` without a password confirmation. Just copy the file in your polkit policy folder '/usr/share/polkit-1/actions'.

Open your terminal and execute `cd /usr/share/polkit-1/actions && sudo wget https://raw.githubusercontent.com/pepe386/fedora-update/master/org.freedesktop.policykit.pkexec.fedora-update.policy`

## Credits
Forked from https://github.com/RaphaelRochet/arch-update and https://github.com/julio641742/fedora-update

Some parts have been taken from the Gnome Extension [apt-update-indicator](https://github.com/franglais125/apt-update-indicator)
