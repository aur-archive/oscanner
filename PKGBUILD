# Archtrack maintainer: Evan Teitelman <teitelmanevan at gmail dot com>
# Contributor: Francesco Piccinno <stack.box@gmail.com>

pkgname=oscanner
pkgver=1.0.6
pkgrel=1
pkgdesc="Oscanner is an Oracle assessment framework developed in Java."
arch=(any)
url="http://www.cqure.net/wp/oscanner/"
updateurl="http://www.cqure.net/wp/oscanner/=>oscanner-"
license=('GPL')
depends=('java-runtime')
source=(http://www.cqure.net/tools/${pkgname}_bin_${pkgver//./_}.zip)
md5sums=('e85138c3cb60b3c6edc997a2160e0576')

groups=(archtrack archtrack-vulnerability-analysis)

build() {
  cd "$srcdir/${pkgname}_bin"
  chmod -R -x *
  chmod +x *.sh *.exe
  find . -type d -exec chmod +x {} \;
  mkdir -p $pkgdir/usr/share/$pkgname/
  cp -r * $pkgdir/usr/share/$pkgname/
}

