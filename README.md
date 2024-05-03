```
wget https://geo.mirror.pkgbuild.com/iso/2024.05.01/archlinux-2024.05.01-x86_64.iso
```
```
wget https://bin.equinox.io/c/bNyj1mQVY4c/ngrok-v3-stable-linux-amd64.tgz
```
```
tar -xf ngrok-v3-stable-linux-amd64.tgz
```
```
rm -rf ngrok-v3-stable-linux-amd64.tgz
```
```
./ngrok config add-authtoken 2fRE7RF60BZ3gkKpQB2TLP23nmM_31VnYfMv2m5Sa4pFjc5wG
```
```
./ngrok tcp 5900
```
```
sudo apt update && apt install qemu-kvm
```
```
sudo qemu-img create -f raw 1.img 64G
```
```
sudo qemu-system-x86_64 -m 8G -cpu host -boot order=c -drive file=archlinux-2024.05.01-x86_64.iso,media=cdrom -drive file=1.img,format=raw -device usb-ehci,id=usb,bus=pci.0,addr=0x4 -device usb-tablet -vnc :0 -smp cores=2 -device rtl8139,netdev=n0 -netdev user,id=n0 -vga qxl -enable-kvm
```
```
rm -rf archlinux-2024.05.01-x86_64.iso
```
```
sudo qemu-system-x86_64 -m 8G -cpu host -boot order=c -drive file=1.img,format=raw -device usb-ehci,id=usb,bus=pci.0,addr=0x4 -device usb-tablet -vnc :0 -smp cores=2 -device rtl8139,netdev=n0 -netdev user,id=n0 -vga qxl -enable-kvm
```
