# Maintainer: Amadeus Folego aka badosu <amadeusfolego at gmail dot com>
pkgname=asuskblctl
pkgver=0.1
pkgrel=1
pkgdesc="Adjust keyboard backlight on Asus laptops"
arch=(any)
url="https://github.com/badosu/asuskblctl"
license=('GPL')
source=(
  https://github.com/badosu/asuskblctl/raw/master/scripts/asuskblctl
  https://github.com/badosu/asuskblctl/raw/master/scripts/asuskblperm
  https://github.com/badosu/asuskblctl/raw/master/systemd/asuskblperm.service)
sha256sums=(
  '52f3882e81de0a1c3d60d3b0e9600d76e2ae493e4bdbd7cd8b2e7210f99f983c'
  'b5afba03bded8470708a6caa1ee233b9e2e00595a01797305970230e956b5ce4'
  'f14eb94eecd14465bc670524d39d0f374ad145c134886ab0cfe68812d51bb28b')

package() {
  cd $srcdir
  install -Dm755 asuskblctl $pkgdir/usr/bin/asuskblctl
  install -Dm755 asuskblperm $pkgdir/usr/bin/asuskblperm
  install -Dm644 asuskblperm.service "${pkgdir}$(pkg-config systemd --variable=systemdsystemunitdir)/asuskblperm.service"
}

# vim: set ts=2 sw=2 et:
