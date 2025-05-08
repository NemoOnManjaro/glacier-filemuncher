# $Id$
# Contributor: TheKit <nekit1000 at gmail.com>
# Contributor: Bart Ribbers <bribbers@disroot.org>
# Contributor: Alexey Andreyev <aa13q@ya.ru>
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=glacier-filemuncher
pkgver=0.5
pkgrel=1
pkgdesc="The Glacier file manager"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-filemuncher"
license=('BSD-3-Clause')
depends=('qt6-glacier-app'
	'nemo-qml-plugin-settings'
	'nemo-qml-plugin-folderlistmodel')
makedepends=('cmake' 'qt6-tools' 'clang')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('5caf585c1a23d75179d924605201d0b66ee9a7784c847201f8238c1fd0682c42')

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
