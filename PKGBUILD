# Maintainer: NAHO <90870942+trueNAHO@users.noreply.github.com>

pkgname=grub-theme-vimix-very-dark-blue
pkgver=1.0.0
pkgrel=1
pkgdesc="Simple very dark blue GRUB theme"
arch=(any)
url="https://github.com/trueNAHO/grub2-theme-vimix-very-dark-blue"
license=(GPL3)
depends=(grub)
makedepends=(git)
optdepends=('grub-customizer: GUI tool to configure GRUB')
source=("git+$url")
md5sums=('SKIP')

pkgver() {
  printf "1.0.0.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
  cd "$srcdir/$pkgname" || return
}

package() {
  install -dm 755 "$pkgdir/usr/share/grub/themes/$pkgname"
  cp -r --no-preserve=ownership grub2-theme-vimix-very-dark-blue/src/. \
      "$pkgdir/usr/share/grub/themes/$pkgname"
}
