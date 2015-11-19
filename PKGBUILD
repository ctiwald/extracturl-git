# Maintainer: Christopher Tiwald <christiwald at gmail dot com>

_pkgname=extracturl
pkgname=extracturl-git
pkgver=4b515b3
pkgrel=1
pkgdesc="Replacement for urlview to parse URL links from mail messages."
url="https://github.com/m3m0ryh0l3/extracturl"
arch=('any')
license=('BSD')
depends=('perl-mime-tools' 'perl-html-parser')
source=(git://github.com/m3m0ryh0l3/extracturl)
md5sums=('SKIP')

pkgver() {
  cd $_pkgname
  git describe --always | sed -e 's|-|.|g' -e 's|v||'
}

build() {
  cd $_pkgname
  make
}

package() {
  cd $_pkgname
  make DESTDIR="$pkgdir" install
}
