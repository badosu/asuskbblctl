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
  https://github.com/badosu/asuskblctl/raw/master/systemd/asuskblperm.service)
sha256sums=(
  '9840573cb17745ff87c4ab1e71b57d450e7232a67b4928108979e2c8690923f6'
  'ba36966ecb74b083c4be455250d808fe9978779489c15814fa1d09798f3ae758'
)

package() {
  cd $srcdir
  install -Dm755 asuskblctl $pkgdir/usr/bin/asuskblctl
  install -Dm644 asuskblperm.service "${pkgdir}$(pkg-config systemd --variable=systemdsystemunitdir)/asuskblperm.service"
}

# vim: set ts=2 sw=2 et:
