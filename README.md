<b>KALI NETHUNTER INSTALLATION FILES FOR LG V10 H901 ONLY</b>
########################################################################################################################
This repository includes a pre-compiled boot.img with a kernel modified to work with most of the features in Kali Linux.

I AM NOT RESPONSIBLE FOR A BRICKED DEVICE, SO READ THE REQUIREMENTS CAREFULLY AND PROCEED AT YOUR OWN RISK!
REMEMBER TO TAKE TWRP BACKUPS OF SYSTEM AND BOOT JUST IN CASE.
If boot.img fails, reboot to twrp using button combination and restore a backup.

Added features include:
> SYSV IPC support (for sysv, fakeroot, etc.)
> Auto mount DEVTMPFS (for features like udev support)
> USB HID emulation
> DVB-T drivers for RTL2832U based SDR dongles
> Ralink USB wireless drivers for Alfa WUSB036 Series WiFi dongles 
> More optimizations, and more to come!

########################################################################################################################
REQUIREMENTS:
> Unlocked bootloader
> TWRP Custom recovery
> Rooted stock v30c ROM (Magisk recommended)
> USB OTG adapter for Alfa wireless cards (recommended)

########################################################################################################################
INSTRUCTIONS: (Follow in this exact order)

Installing the NetHunter Kernel:
1. Restart your phone into TWRP
2. Tap "Install"
3. On the bottom right, tap "Install Image"
4. Browse to where you extracted this git repository.
5. Select "boot.img"
6. Under partiton type, select "Boot"
7. Swipe to install

Installing the NetHunter binaries/base rootfs:
1. After installing boot image, navigate back to the main menu
2. Tap "Install"
3. On the bottom right, tap "Install ZIP"
4. Navigate to this repository
5. Tap "nethunter-generic-arm64-install.zip"
6. Swipe to install (be patient, it will take a while. We're not in a hurry here.)
7. Reboot system

After you rebooted back into Android:
1. Open the NetHunter app
2. Under the left menu pane, select "Kali chroot manager"
3. Wait for the chroot to be detected, then tap "Add metapackages". Choose what features you want to install, then
tap "Install&Update". (NOTE: This will take a very long time!)
4. Enjoy a powerful portable penetration testing tool!

BUGS:
> Sometimes when using rtl_tcp, a kernel panic will occur.
> Wifite will not open the wlan1mon interface, even if airmon-ng start wlan1 is ran.
