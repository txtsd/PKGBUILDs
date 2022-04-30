# Maintainer: Dawson Dias <thexerothermicsclerodermoid@gmail.com>
# Contributor: Jacob Gogichaishvili <jggsecondary@gmail.com>

_pkgname="zaread"
pkgname="$_pkgname-git"
pkgver=r47.9239db1
pkgrel=2
pkgdesc="A (very) lightweight ebook and Office document reader"
arch=("any")
url="https://github.com/paoloap/zaread"
license=("GPL")
depends=("zathura")
optdepends=("libreoffice" "calibre" "md2pdf")
provides=("zaread")
conflicts=("zaread")
source=('git+https://github.com/paoloap/zaread.git')
sha256sums=('SKIP')

pkgver() {
  cd "$srcdir/$_pkgname"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  cd "$srcdir/$_pkgname"
  mkdir -p "$pkgdir/${PREFIX:-usr}/bin"
  install -Dm755 "$srcdir/$_pkgname/$_pkgname" "$pkgdir/${PREFIX:-usr}/bin/"
  install -Dm644 LICENSE -t "$pkgdir/usr/share/licenses/$_pkgname/"
  install -Dm644 README.md -t "$pkgdir/usr/share/doc/$_pkgname/"
}
