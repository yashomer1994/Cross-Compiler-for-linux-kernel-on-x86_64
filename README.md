# Cross-Compiler-for-linux-kernel-on-x86_64

# Tutorial to build Cross Compiler for Linux kernel on x86_64 Systems

This Respoistory is used To build CROSS COMPILATION for different architectures for Linux Kernel On Ubuntu.

The host environment used for cross compilation is Ubuntu - 18.04.

Ubuntu Arm packages used are : -

gcc-arm-linux-gnueabi
gcc-arm-linux-gnueabihf

For Cross Compiler packages we are going to use Fedora packages as Debian.

Download these rpm's from Fedora portal for easy download.

blackfin:
binutils-bfin-linux-gnu.rpm (any version)
gcc-bfin-linux-gnu.rpm (any version)

c6x:

binutils-c6x-linux-gnu.rpm ( any version)
gcc-c6x-linux-gnu.rpm(any version)

tile:
bintuils-tile-linux-gnu.rpm( any version)
gcc-tile-linux.rpm(any version)


For the installation of cross-compilation you can use  Ubuntu version 

Note: Do Install these packages for Linux Kernel Compilation.

sudo apt-get install build-essential
sudo apt-get install ncurses-dev
sudo apt-get install multi-arch
sudo apt-get install alien


Convert RPM To DEB

sudo alien -d binutils-bfin-linux-gnu.rpm (any version)
sudo alien -d gcc-bfin-linux.gnu.rpm (any version)

sudo alien -d binutils-c6x-linux-gnu.rpm (any version)
sudo alien -d gcc-c6x-linux-gnu.rpm (any version

sudo alien -d binutils-tile-linux-gnu.rpm (any version)
sudo alien -d gcc-tile-linux-gnu.rpm( any version)


The Following .debs file will created :-

binutils-bfin-linux-gnu_amd64.deb
gcc-bfin-linux-gnu_amd64.deb

binutils-c6x-linux-gnu_amd64.deb
gcc-c6x-linux-gnu_amd64.deb

binutils-tile-linux-gnu_amd64.deb
gcc-tile-linux.gnu_amd64.deb

INSTALLATION:
1. ARM:
sudo apt-get install gcc-arm-linux-gnueabi

2. ARM64:

sudo apt-get install gcc-aarch64-linux-gnu
sudo ln -s /usr/bin/aarch64-linux-gnueabi-gcc-7 /usr/bin/aarch64-linux-gnu-gcc

3. ALPHA:
sudo apt-get install gcc-alpha-linux-gnu
sudo ln -s /usr/bin/alpha-linux-gnueabi-gcc-7 /usr/bin/alpha-linux-gnu-gcc

For Cross Compilation Download Linux kernel from https://www.kernel.org untar using
