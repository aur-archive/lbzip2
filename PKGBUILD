# Maintainer: Jaroslav Lichtblau <dragonlord@aur.archlinux.org>
# Contributor: Christoph Zeiler <archNOSPAM_at_moonblade.dot.org>

pkgname=lbzip2
pkgver=2.5
pkgrel=2
pkgdesc="A parallel, SMP-based, bzip2-compatible compression utility"
arch=('i686' 'x86_64')
url="http://freecode.com/projects/lbzip2"
license=('GPL' 'GPL3')
#depends=('bzip2')
makedepends=('autoconf' 'automake' 'perl' 'gnulib-git' 'gcc')
source=($pkgname-$pkgver.tar.gz::https://github.com/kjn/$pkgname/tarball/v$pkgver)
sha256sums=('aa4af0c2e01db74d3dec139f4d8d6e24aee669701ef3e7cd306344bd147a6c90')

build() {
  cd kjn-$pkgname-*

  ./build-aux/autogen.sh	
  ./configure --prefix=/usr
  make
}

package() {
  cd kjn-$pkgname-*

  make DESTDIR="${pkgdir}" install
}
