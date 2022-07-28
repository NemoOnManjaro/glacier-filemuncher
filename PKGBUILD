# $Id$
# Contributor: TheKit <nekit1000 at gmail.com>
# Contributor: Bart Ribbers <bribbers@disroot.org>
# Contributor: Alexey Andreyev <aa13q@ya.ru>
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=glacier-filemuncher
pkgver=0.3.2
pkgrel=1
pkgdesc="The Glacier file manager"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-filemuncher"
license=('BSD-3-Clause')
depends=('qt5-glacier-app'
	'nemo-qml-plugin-settings'
	'nemo-qml-plugin-folderlistmodel')
makedepends=('cmake' 'qt5-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('c7b9f59a28b9de289be026eb1ec7c352837e4fce55af2ff0e02793ff46cfbc65')

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
