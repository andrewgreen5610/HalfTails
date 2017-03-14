
## Installation of HalfTails from Ubuntu, Debian or Mint

Step-by-step at terminal.

**Step-1**: get the ISO and check it (~15 minutes to download).

```sh
# the halfTail elected ISO image:
 wget -c http://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/debian-live-8.7.1-amd64-gnome-desktop.iso

# the checksums for it:
 wget -c http://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/SHA256SUMS
 # need certificate?  SHA256SUMS.sign
 sha256sum -c SHA256SUMS 2>&1 | grep -E 'OK|SUCESSO' 
 # debian-live-8.7.1-amd64-standard.iso: OK
```

**Step-2**: check and/or install `mkusb`
If `mkusb --version`  is old or not exist,  

```
# sudo add-apt-repository universe  # somente para "standard Ubuntu" (em geral já está la)
sudo add-apt-repository ppa:mkusb/ppa  # e tecle Enter
sudo apt-get update # aguarde antes do proximo comando
sudo apt-get install mkusb mkusb-nox usb-pack-efi  # aguarde ... 
mkusb --version  # tudo ok? siga.
```

....
