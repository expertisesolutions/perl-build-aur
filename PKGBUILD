# Maintainer: Felipe Magno de Almeida <felipe.m.almeida__at__gmail.com>

pkgbase=build
pkgname=perl-build
pkgver=20160615
pkgrel=1
pkgdesc="Tizen's Build.pm project"
arch=('i686' 'x86_64')
license=('GPL')
makedepends=('perl')
depends=('perl' 'perl-yaml' 'perl-html-template' 'perl-json')
source=('git://git.tizen.org/tools/build.git' 'destdir.patch')
sha256sums=('SKIP' '7016fc7df0919d2ca76131593d7b42e69e5c9d2376e8f28ab9558d620a474159')

build() {
  cd $srcdir/build
  patch -p1 -i ../../destdir.patch
}

package() {
  cd $srcdir/build
  DESTDIR=$pkgdir make install
#  install -m644 -D LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE
}
