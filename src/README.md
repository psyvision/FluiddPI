Build VCoreOS From within VCoreOS / FluiddPI / OctoPi / Raspbian / Debian / Ubuntu
VCoreOS can be built from Debian, Ubuntu, Raspbian, OctoPi, or even VCoreOS. Build requires about 5 GB of free space available. You can build it by issuing the following commands:

```bash
sudo apt-get install gawk util-linux qemu-user-static git p7zip-full python3

git clone https://github.com/guysoft/CustomPiOS.git
git clone https://github.com/Rat-Rig/V-CoreOS.git
cd V-CoreOS/src/image
wget -c --trust-server-names 'https://downloads.raspberrypi.org/raspios_lite_armhf_latest'
cd ..
../../CustomPiOS/src/update-custompios-paths
sudo modprobe loop
sudo bash -x ./build_dist
```