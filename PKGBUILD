# Contributer: giacomogiorgianni@gmail.com

pkgname=harbour
pkgver=3.0.0
pkgrel=2
license=('GPL3')
arch=('any')
depends=('qt4' 'zlib' 'libjpeg-turbo' 'pcre' 'libpng12' 'lib32-sqlite3' 'openssl' 'ncurses' 'gpm' 'libx11' 'slang')
pkgdesc="Compiler for the xBase superset language often referred to as Clipper Harbour is a free software compiler for the xBase superset language"
url="http://sourceforge.net/projects/harbour-project/?source=directory"
makedepends=('gcc' 'pkgconfig' )
conflicts=('')
options=(!emptydirs)
source=(http://dfn.dl.sourceforge.net/project/harbour-project/source/$pkgver/$pkgname-$pkgver.tar.bz2)

md5sums=('ebcdaba3dfe86f1f67b3a78806b85a78')

build() {
  cd $srcdir/$pkgname-$pkgver
  make
  rm ./lib/linux/gcc/libexpat.a
  make DESTDIR=$pkgdir install
  #Conflict expat
  rm  $pkgdir/lib/libexpat.a
}
