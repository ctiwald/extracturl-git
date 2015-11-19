_pkgname=extracturl
pkgname=extracturl-git
pkgver=1.6.4b515b30
pkgrel=1
pkgdesc="Replacement for urlview to parse URL links from mail messages."
url="https://github.com/m3m0ryh0l3/extracturl"
arch=('any')
license=('SKIP')
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
