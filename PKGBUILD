# $Id$

pkgname=glacier-weather
pkgver=0.1
pkgrel=1
pkgdesc="Nemo weather"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-weather"
license=('BSD-3-Clause' 'LGPL-2.1-only')
depends=('qt5-glacier-app' 'qt5-location')
makedepends=('cmake' 'qt5-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('47ec709e09829996245ea8f8bf771f2c2301c54673c81a5ee2cee85e1aaa4bef')

build() {
    cd $pkgname-$pkgver
    cmake \
        -DCMAKE_INSTALL_PREFIX:PATH='/usr'
    make all
}


package() {
    cd $pkgname-$pkgver
    make DESTDIR="$pkgdir" install
}
