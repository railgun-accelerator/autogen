# $Id$
# Maintainer: Jan de Groot <jgc@archlinux.org>
# Contributor: Arjan Timmerman <arjan@soufly.nl>
# Contributor: Tor Krill

pkgname=autogen
pkgver=5.18.6
pkgrel=1
pkgdesc="A tool designed to simplify the creation and maintenance of programs that contain large amounts of repetitious text"
arch=('i686' 'x86_64')
url="http://www.gnu.org/software/autogen/"
license=('GPL3')
depends=('guile' 'libxml2')
install=autogen.install
source=(http://ftp.gnu.org/gnu/${pkgname}/rel${pkgver}/${pkgname}-${pkgver}.tar.xz)
md5sums=('db0a9594979200a99d286aa85d492d21')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
} 
