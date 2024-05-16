# $Id$

pkgname=glacier-weather
pkgver=0.2
pkgrel=1
pkgdesc="Nemo weather"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-weather"
license=('BSD-3-Clause' 'LGPL-2.1-only')
depends=('qt6-glacier-app' 'qt6-location')
makedepends=('cmake' 'qt6-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('f7f1fb8933b2c250762636a3b9f02697800faa602539a633923c837eb06af096')

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
