
### 1. Build linuxcnc

sudo apt-get -y install git autoconf libudev-dev libmodbus-dev libusb-1.0-0-dev libglib2.0-dev tcl-dev tk-dev bwidget libtk-img tclx8.4 libgtk-3-dev libreadline-gplv2-dev python-tk libboost-all-dev screen libboost-all-dev python-opengl libglu1-mesa-dev libxmu-dev yapps2  libgtk2.0-dev intltool

git clone git://github.com/linuxcnc/linuxcnc.git linuxcnc-dev

cd linuxcnc/src

./autogen.sh

#./configure --with-realtime=uspace --disable-gtk --enable-non-distributable=yes --disable-python

./configure --with-realtime=uspace --enable-non-distributable=yes

make -j4

sudo make setuid

cd ~/linuxcnc

. scripts/rip-environment

linuxcnc

### 2. Build Ethercat Master

### 3. Build Ethercat for LinuxCNC
