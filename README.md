# Bluetooth bug fix for kernel patch 

Bluetooth: hci0: don't support firmware rome 0x11020000

Ubuntu 4.15 bluetooth source code patched with https://bugzilla.opensuse.org/attachment.cgi?id=770190 [*TakashiIwai]


Should fix Ubuntu Bug https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1764645

* To use : FOLLOW THE STEPS GIVEN BELOW:

=====================================================================

Debian/Ubuntu:

```
sudo apt install build-essential git dkms
```


Fedora:

```
sudo dnf install make automake gcc gcc-c++ kernel-devel git dkms
```

```

git clone https://github.com/lvitals/bluetooth-btusb-fix.git

sudo mkdir /usr/src/btusb-4.0

sudo cp bluetooth-btusb-fix/* /usr/src/btusb-4.0/

sudo dkms install btusb/4.0 

```


Reboot and check the bluetooth setting (It'll be working)

=====================================================================
