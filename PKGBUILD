# Maintainer: Kevin Del Castillo R. <lans9831@gmail.com>

pkgname=search-in-dir-git
pkgver=1.1
pkgrel=1
pkgdesc="ディレクトリの中のテキストファイルを検索します。"
arch=('any')
url=https://github.com/Hayao0819/search-in-dir
license=('MIT')
depends=('zenity' 'jq' 'bash')
optdepends=()
source=("git+https://github.com/Hayao0819/search-in-dir.git")
md5sums=('SKIP')
conflicts=()

pkgver() {
  cd "search-in-dir"

  git describe --tags | sed 's/-/.r/; s/-g/./'
}

build () {
  cd "search-in-dir"
  rm -f README.md
  rm -f PKGBUILD
  rm -rf .git
}
package() {
    mkdir -p "$pkgdir"
    cp -r * "$pkgdir"
}

