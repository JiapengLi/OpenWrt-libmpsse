# OpenWrt-libmpsse

OpenWrt patch for libmpsse https://code.google.com/p/libmpsse/

## How To

	cd ~
	git clone https://github.com/JiapengLi/OpenWrt-libmpsse.git
	cd openwrt/trunk
	./scripts/feeds update -a
	./scripts/feeds install -a
	cd feeds/packages
	patch -p1 < ~/OpenWrt-libmpsse/openwrt-add-support-for-libmpsse.patch
	./scripts/feeds update -i
	./scripts/feeds install libmpsse
	
	make menuconfig
	// choose the right platform
	// Select libmpsse in Libraries --> libmpsse

	make

## Build Single Package

	make package/libmpsse/compile V=s
	make package/libmpsse/install V=s
	make package/index

## Useful Links

[Write and cmopile a simple package for OpenWrt](http://www.gargoyle-router.com/wiki/doku.php?id=openwrt_coding)  
[Create Package](http://wiki.openwrt.org/doc/devel/packages)  
[Build Single Package](http://wiki.openwrt.org/doc/howtobuild/single.package)  
[Building your own package for OpenWRT](http://vivekian2.wordpress.com/2007/03/28/building-your-own-package-for-openwrt/)
