# Contributor: arjan <arjan@archlinux.org>
# Contributor: Sarah Hay <sarahhay@mb.sympatico.ca>
# Maintainer: Anton Larionov <diffident dot cat at gmail dot com>

pkgname=lincity
pkgver=1.13.1
pkgrel=2
pkgdesc="A free construction and management simulation game"
arch=('i686' 'x86_64')
url="http://lincity.sourceforge.net/"
license=('GPL')
depends=('libpng' 'libx11')  # 'libxext' 'libsm'
source=(http://downloads.sourceforge.net/sourceforge/lincity/${pkgname}-${pkgver}.tar.gz)
md5sums=('2d37906d4b141cd457ec93d778bb8fe1')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr --mandir=/usr/share/man
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
  rmdir "${pkgdir}/usr/lib"
}

# vim:set ts=2 sw=2 et:
