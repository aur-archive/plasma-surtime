# Maintainer: Tomasz 'ludvick' Niedzielski <ludvick0[AT]gmail[DOT]com>

pkgname=plasma-surtime
pkgver=1.0.0
pkgrel=1
pkgdesc="collection of analog and digital clocks"
arch=('any')
url="http://kde-apps.org/usermanager/search.php?username=surbiks"
license=('GPL')
install=${pkgname}.install
source=('http://kde-apps.org/CONTENT/content-files/153555-plasma-SurTime_1.0.0.tar.gz')
depends=('kdebase-workspace')
makedepends=('cmake' 'make')
md5sums=('61cbc994b8fabcb0e39030ca0f4e0c45')

build() {
	cd ${srcdir}/${pkgname}_${pkgver}

	cmake -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix`
	make
}

package() {
	cd ${srcdir}/${pkgname}_${pkgver}

	make DESTDIR=${pkgdir} install

	mkdir -p ${pkgdir}/usr/share/icons/hicolor
	mv ${pkgdir}/usr/share/icons/surtime_icon.png ${pkgdir}/usr/share/icons/hicolor/surtime_icon.png
}

