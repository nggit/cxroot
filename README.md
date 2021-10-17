# cxroot
chroot into a Linux rootfs. For Android devices that have been rooted, be it using Magisk or other methods. Tested on an Android One device.
## Prerequisites
Get the Linux rootfs easily from:
```
https://uk.images.linuxcontainers.org/images/
```
If the link is not accessible, there are several mirrors available out there:
```
https://mirrors.tuna.tsinghua.edu.cn/lxc-images/images/
https://mirrors.cloud.tencent.com/lxc-images/images/
```
Make sure you choose the correct architecture and then extract it under `/data/rootfs/distro`.
## Usage
```
./cxroot /data/rootfs/distro
./cxroot distro
./cxroot /data/another/path/distro
```
## Example
Let's create a chroot environment based on Alpine Linux...
```
# Download Alpine Linux rootfs (2.8M)
wget https://uk.images.linuxcontainers.org/images/alpine/3.14/arm64/default/20211016_13:00/rootfs.tar.xz

su
mkdir -p /data/rootfs/alpine

# Extract rootfs.tar.xz to /data/rootfs/alpine
tar -xvf rootfs.tar.xz -C /data/rootfs/alpine

# Download cxroot script
wget https://raw.githubusercontent.com/nggit/cxroot/master/cxroot
chmod +x cxroot

# Enter Alpine Linux chroot environment
./cxroot /data/rootfs/alpine

# Exit Alpine Linux chroot environment
exit
```
## Screenshot
![cxroot](cxroot.png)
