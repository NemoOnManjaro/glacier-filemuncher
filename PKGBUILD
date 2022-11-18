# $Id$
# Contributor: TheKit <nekit1000 at gmail.com>
# Contributor: Bart Ribbers <bribbers@disroot.org>
# Contributor: Alexey Andreyev <aa13q@ya.ru>
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=glacier-filemuncher
pkgver=0.3.3
pkgrel=1
pkgdesc="The Glacier file manager"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-filemuncher"
license=('BSD-3-Clause')
depends=('qt5-glacier-app>=0.9'
	'nemo-qml-plugin-settings'
	'nemo-qml-plugin-folderlistmodel')
makedepends=('cmake' 'qt5-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('c3c424955a7dcc241e2b3e624257197142162c45757e34036dab6c1a51d4334f')

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
