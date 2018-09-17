pkgname=st
pkgver=0.8.1
pkgrel=1
pkgdesc="My own fork of st"
url="https://st.suckless.org/"
arch=('x86_64')
license=('MIT')
license=('GPL')
depends=('libxext' 'libxft')
provides=(st)
conflicts=(st)

source=()
md5sums=()

builddir=$(pwd)

build() {
  cd $builddir
	make
}

package() {
  cd $builddir
	make DESTDIR="$pkgdir" PREFIX=/usr install
	install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
