# Maintainer: kreed <kreed@kreed.org>
# Contributor: loonyphoenix <loonyphoenix at gmail>

pkgname=smplayer2
pkgver=0.8.0
pkgrel=2
pkgdesc="A fork of SMPlayer, targeted at mplayer2 users"
url="https://github.com/lachs0r/SMPlayer2"
arch=('i686' 'x86_64')
license=('GPL')
depends=('qt4' 'mplayer2')
makedepends=('cmake')
optdepends=('quazip: rebuild with this AUR library installed for Subtitle Downloader support')
source=("https://github.com/lachs0r/SMPlayer2/archive/v${pkgver}.tar.gz")

build() {
  cd "SMPlayer2-$pkgver"
  cmake -DCMAKE_INSTALL_PREFIX=/usr -DQT_QMAKE_EXECUTABLE=qmake-qt4 .
  make
}

package() { 
  cd "SMPlayer2-$pkgver"
  make DESTDIR="$pkgdir" install
}

sha256sums=('ebb8c433c47cb2d5f5f97b4ea4791eb21f8aeb1ad6b17f4dd120bb97f2d5860e')
