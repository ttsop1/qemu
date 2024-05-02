```
wget https://github.com/manjaro-arm/generic-images/releases/download/23.02/Manjaro-ARM-xfce-generic-23.02.img.xz
```
```
xz -d Manjaro-ARM-xfce-generic-23.02.img.xz
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
sudo qemu-system-aarch64 -m 8G -cpu cortex-a57 -M virt -boot order=c -drive file=Manjaro-ARM-xfce-generic-23.02.img,format=raw -device usb-ehci,id=usb,bus=pci.0,addr=0x4 -device usb-tablet -vnc :0 -smp cores=2 -device rtl8139,netdev=n0 -netdev user,id=n0 -vga qxl -enable-kvm
```
