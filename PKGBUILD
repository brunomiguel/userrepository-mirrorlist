# Maintainer: Bruno Miguel <brunoalexandremiguel@gmail.com>

pkgname=userrepository-mirrorlist
pkgver=0.0.2
pkgrel=1
pkgdesc="Userrepository.eu mirror list for pacman"
arch=('any')
url="https://raw.githubusercontent.com/brunomiguel/userrepository-mirrorlist/main/"
license=('GPL')
backup=(etc/pacman.d/userrepository-mirrorlist)
source=(mirrorlist)
install=userrepository.install

# NOTE on building this package:
# * Go to the trunk/ directory
# * Run bash -c ". PKGBUILD; updatelist"
# * Update the checksums, update pkgver
# * Build the package

updatelist() {
  rm -f mirrorlist
  curl -o mirrorlist "$url/mirrorlist"
}

package() {
  mkdir -p "$pkgdir/etc/pacman.d"
  install -m644 "$srcdir/mirrorlist" "$pkgdir/etc/pacman.d/userrepository-mirrorlist"
}

sha256sums=('c27836273386f23e2cf0ff5be2a76701adcc51a3b55ab97381299e911786c64d')

