# $Id$
# Contributor: TheKit <nekit1000 at gmail.com>
# Contributor: Bart Ribbers <bribbers@disroot.org>
# Contributor: Alexey Andreyev <aa13q@ya.ru>
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=glacier-filemuncher
pkgver=0.4
pkgrel=2
pkgdesc="The Glacier file manager"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-filemuncher"
license=('BSD-3-Clause')
depends=('qt6-glacier-app'
	'nemo-qml-plugin-settings'
	'nemo-qml-plugin-folderlistmodel')
makedepends=('cmake' 'qt6-tools' 'clang')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('97d60761cd87044819fd195ae6fb94d1b0a41f622296b2542190815237a0a69a')

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
