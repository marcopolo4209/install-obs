# Update OS
yum update

# INSTALL REPOSITORY
yum install epel-release
yum localinstall --nogpgcheck https://download1.rpmfusion.org/free/el/rpmfusion-free-release-7.noarch.rpm https://download1.rpmfusion.org/nonfree/el/rpmfusion-nonfree-release-7.noarch.rpm

# INSTALL FFMPEG
yum install ffmpeg ffmpeg-devel

# INSTALL BUILD PACKAGES
yum  install gcc gcc-c++ gcc-objc cmake git


# INSTALL REQUIRED PACKAGES
yum install -y libX11-devel 
yum install -y mesa-libGL-devel 
yum install -y libv4l-devel \
yum install -y pulseaudio-libs-devel 
yum install -y x264-devel 
yum install -y freetype-devel
yum install -y fontconfig-devel 
yum install -y libXcomposite-devel 
yum install -y libXinerama-devel
yum install -y qt5-qtbase-devel 
yum install -y qt5-qtx11extras-devel 
yum install -y libcurl-devel
yum install -y systemd-devel
yum install -y luajit-devel 
yum install -y swig 
yum install -y python36-devel


# BUILDING and INSTALLING OBS
cd /tmp
git clone --recursive https://github.com/obsproject/obs-studio.git
cd obs-studio
mkdir build && cd build
cmake -DUNIX_STRUCTURE=1 ..
make -j4
sudo make install


# CREATE CONFIG FILE
gedit /etc/ld.so.conf.d/local.conf

# add this line in file:
/usr/local/lib

#and run
ldconfig

# TO START RUN
obs
