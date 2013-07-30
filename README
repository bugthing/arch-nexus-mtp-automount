Auto mount a Nexus device in Arch
=================================

There is likely a better way to do this, but this is how I auto mount my Nexus
devices in Arch Linux.

    git clone git@github.com:bugthing/arch-nexus-mtp-automount.git

    makepkg -s

    sudo pacman -U android-automount-0.1-1-any.pkg.tar.xz

    cp 99-android-mtp.rules /etc/udev/rules.d/

    cp android-mtp.service 

    sudo systemctl start android-mtp

    sudo systemctl enable android-mtp
