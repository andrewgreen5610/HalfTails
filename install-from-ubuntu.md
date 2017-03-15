
## Installation of HalfTails from Ubuntu, Debian or Mint

HalfTails is the Live USB Debian system obtained after a sequence of steps and using some good-practices. 

Step-by-step at terminal. Minimal pendrive 2Gb.

**Step-1**: get the ISO and check it (~15 minutes to download).

```sh
# the halfTail elected ISO image:
 wget -c http://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/debian-live-8.7.1-amd64-gnome-desktop.iso

# the checksums for it:
 wget -c http://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/SHA512SUMS
 # need certificate?  SHA256SUMS.sign
 sha512sum -c SHA512SUMS 2>&1 | grep -E 'OK|SUCESSO' 
 # debian-live-8.7.1-amd64-standard.iso: OK
```

**Step-2**: check and/or install `mkusb`
If version by `man mkusb | tail`, need be "version 12.0.0" or newer. If old purge with `

```sh
# sudo add-apt-repository universe  # only for "standard Ubuntu" (may be there)
sudo add-apt-repository ppa:mkusb/ppa  # press Enter
sudo apt-get update # wait to the next command
sudo apt install mkusb mkusb-nox usb-pack-efi  # wait ... 
man mkusb | tail | grep version  # it is 12.0.0?
```

**Step-3**: make your pendrive Live USB!

Only answer pressing letters or buttons after initial command.

```sh
mkusb
# them, press "d" for mkusb-dus  interface
# at first popup click "i" and OK button
# at second popup click "p" or "l" as your preference.
```
## Optional to change terminal language

see https://superuser.com/a/647957

## under construction
* at persistent pendrive, *purge* sumeting to go faster at boot?  
* purge something to avoid risk?  
* ...

## general best practices

See [the Wiki](https://github.com/CidadeAmarela/HalfTails/wiki/Best-Practices). 
