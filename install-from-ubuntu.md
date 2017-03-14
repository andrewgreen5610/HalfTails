
## Installation of HalfTails from Ubuntu, Debian or Mint

Step-by-step at terminal.

```sh
# the halfTail elected ISO image:
 wget -c http://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/debian-live-8.7.1-amd64-gnome-desktop.iso

# the checksums for it:
 wget -c http://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/SHA256SUMS
 # need certificate?  SHA256SUMS.sign
 sha256sum -c SHA256SUMS 2>&1 | grep -E 'OK|SUCESSO' 
 # debian-live-8.7.1-amd64-standard.iso: OK
...
```
