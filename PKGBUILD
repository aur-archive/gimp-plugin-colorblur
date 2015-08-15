# Contributor: Tibor Bamhor <tiborb95 at gmail.com>

pkgname=gimp-plugin-colorblur
pkgver=0.6.2 
pkgrel=1
pkgdesc="Color-based blur. Similar to standard Selective Blur plugin but with more options. Intended to fix/enhance poorly saturated images or cartoonization."
url="http://code.google.com/p/cartooner-color-reducer/"
license="GPL3"
arch=('i686' 'x86_64')
depends=(gimp)
#makedepends=()
source=(http://selective-color-blur.googlecode.com/files/colorblur-${pkgver}.tgz)

build() {
	export LDFLAGS="$LDFLAGS -lm"
	
	cd ${srcdir}/colorblur
	
	gimptool-2.0 --build colorblur.c
}

package() {


	#copying file into pkgdir to be packed
	mkdir -p $pkgdir/usr/lib/gimp/2.0/plug-ins/

	install -m 755 ${srcdir}/colorblur/colorblur $pkgdir/usr/lib/gimp/2.0/plug-ins/ 
	
}

sha1sums=('a608341b01bb0aa394186091819af47c0a5b2b2e') 
