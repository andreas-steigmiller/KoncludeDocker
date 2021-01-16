# This dockerfile makes a snapshot of the development environment
FROM koncluderun

# install build dependencies
RUN apt-get install -y \
apt-utils \
git \
build-essential \
make \
wget \
xz-utils \
python \
flex \
bison \
gperf \
python-dev \
autotools-dev \
automake \
autoconf \
libtool \
gtk-doc-tools \
libgmp3-dev \
zlib1g-dev 






# download, build and install qt
RUN cd /usr/local/src/ \
&& wget https://download.qt.io/official_releases/qt/5.12/5.12.10/single/qt-everywhere-src-5.12.10.tar.xz \
&& tar -xJf qt-everywhere-src-5.12.10.tar.xz \
&& mv qt-everywhere-src-5.12.10 qt-static \
&& cd /usr/local/src/qt-static \
&& export MAKE=/usr/bin/make \
&& ./configure -static -prefix /usr/local/lib/qt-static -extprefix /usr/local/lib/qt-static -no-opengl -nomake examples -nomake tests -opensource -platform linux-g++-64 -no-icu -confirm-license -opensource \
&& make -j \
&& make install





