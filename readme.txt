Introduction:

This codes are TB-96AI board which is designed by Beiqicloud.com. It is available for purchase from Beiqicloud.com.



Get code:

$ mkdir tb-96ai && cd tb-96ai
$ repo init --repo-url http://github.com/aosp-mirror/tools_repo.git -u https://github.com/96boards-tb-96ai/manifest.git

Build envirement:
Host machine OS: Ubuntu 14.04
$sudo apt-get install openjdk-8-jdk 
$sudo update-alternatives --config java
$sudo update-alternatives --config javac
$sudo apt-get install git gnupg flex bison gperf build-essential \
	zip curl libc6-dev libncurses5-dev:i386 x11proto-core-dev \
	libx11-dev:i386 libreadline6-dev:i386 libgl1-mesa-glx:i386 \
	g++-multilib mingw32 tofrodos gcc-multilib ia32-libs \
	python-markdown libxml2-utils xsltproc zlib1g-dev:i386 \
	lzop libssl1.0.0 libssl-dev

Build SDK:

build all:
$./build.sh -b 96ai

only build kernel for android:
$cd kernel
$./make.sh android 96ai
only build kernel for federo linux:
$cd kernel
$./make.sh linux 96ai

Generate firmware in the path:
rockdev/Image-rk3399pro/


