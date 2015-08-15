# $Id: PKGBUILD 215813 2014-06-30 16:22:51Z fyan $
# Maintainer: Tobias Powalowski <tpowa@archlinux.org>

pkgname=capseo
pkgver=0.3
pkgrel=3
epoch=1
pkgdesc="Capseo video codec"
arch=('i686' 'x86_64')
url="https://gitorious.org/capseo"
license=('GPL2')
depends=('libgl' 'gcc-libs')
makedepends=('pkgconfig' 'mesa' 'libogg')
source=("ftp://ftp.archlinux.org/other/capseo/${pkgname}-${pkgver}.tar.gz")
md5sums=('bd869e8c9b1081e90a44567092ea8c5e')

build() {
  cd "${srcdir}"
  ./autogen.sh
  ./configure --prefix=/usr --disable-static
  make
}

package() {
  cd "${srcdir}"
  make DESTDIR="${pkgdir}" install
}
