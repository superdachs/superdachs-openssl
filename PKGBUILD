# $Id: PKGBUILD,v 1.12 2003/11/06 08:26:13 dorphell Exp $
# Maintainer: Stefan Kauerauf <mail@stefankauerauf.de>
# Contributor: Stefan kauerauf <mail@stefankauerauf.de>
pkgname=superdachs-openssl
pkgver=1.1.0
pkgrel=2
pkgdesc="openssl with libs"
arch=(x86_64)
url="https://github.com/superdachs/superdachs-openssl"
license=('GPL')
groups=('')
provides=('')
depends=('')
makedepends=('')
conflicts=('')
replaces=('')
backup=('')
install=''
source=('http://ftp.openssl.org/source/openssl-1.1.0.tar.gz')
md5sums=('dbef70de4a1a4bdd78ab7c6547e5211d')

build() {
    cd ${srcdir}/openssl-${pkgver}
    ./config --prefix="/usr/local/superdachs-openssl" shared
    make -j $(nproc) depend
    make -j $(nproc) all
}

package() {
    cd ${srcdir}/openssl-${pkgver}
    make DESTDIR=$pkgdir install
}
