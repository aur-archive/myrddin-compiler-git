# Maintainer: jmf <jmf at mesecons dot net>

pkgname=myrddin-compiler-git
pkgver=20140712
pkgrel=1
pkgdesc="The Myrddin compiler - git"
options=('staticlibs')
arch=('x86_64')
url="http://eigenstate.org/myrddin"
license=('MIT')
depends=('glibc')
makedepends=('git')
conflicts=('myrddin-compiler')
source=("$pkgname"::'git://github.com/oridb/mc.git')
md5sums=('SKIP')

build() {
  unset CFLAGS
  cd "$srcdir/$pkgname"
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname"
  make DESTDIR="$pkgdir" install
  install -D -m755 LICENSE $pkgdir/usr/share/licenses/myrddin-compiler-git/LICENSE
}

