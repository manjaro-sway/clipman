# Maintainer: Husam Bilal <me@husam.dev>

pkgname=clipman
pkgver=1.6.0
pkgrel=1
pkgdesc="A simple clipboard manager for Wayland"
url="https://github.com/yory8/clipman"
depends=("wl-clipboard>=2.0")
makedepends=("go")
provides=("clipman")
license=("GPL3")
arch=("i686" "x86_64" "arm" "armv6h" "armv7h" "aarch64")
md5sums=("080e00daf96d03564412f8f999f53962")
source=("https://github.com/yory8/${pkgname}/archive/v${pkgver}.tar.gz")

build() {
  cd $pkgname-$pkgver
  go build .
}

package() {
  cd $pkgname-$pkgver
  install -Dm755 $pkgname $pkgdir/usr/bin/$pkgname
  install -Dm644 docs/$pkgname.1 $pkgdir/usr/share/man/man1/$pkgname.1
  gzip $pkgdir/usr/share/man/man1/$pkgname.1
}
