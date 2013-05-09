# Maintainer: Thanh Ha <thanh.ha at alumni.carleton dot ca>
# Contributor: Marcel Huber <marcelhuberfoo at gmail dot com>
#
# Repository: https://github.com/zxiiro/arch-gerrit

pkgname=gerrit
pkgver=2.5.2
pkgrel=2
epoch=
pkgdesc="A web-based code review tool built on top of the git version control system"
arch=(any)
url="http://code.google.com/p/gerrit/"
license=('Apache')
groups=()
depends=(java-runtime ttf-dejavu libcups)
makedepends=()
checkdepends=()
optdepends=('bcprov: Java cryptography APIs (Bouncy Castle)')
provides=()
conflicts=()
replaces=()
backup=(etc/default/gerritcodereview)
options=()
install=gerrit.install
changelog=changelog
source=(gerrit.war::http://gerrit.googlecode.com/files/gerrit-full-$pkgver.war
        gerrit.conf
        gerrit.systemd)
noextract=(gerrit.war)
sha256sums=('20b2ec7e67e0ff65178a5a265b3681bbdf9f1b31b7edb725a0928a58e19088d2'
            '35becf2754e3779c750b2889909349160c2b0584ec201f6cfb5cf2c42e6fc598'
            'be1d205c6a0f3b24aad3c385f8188c64bfa3a9799ecf8ce5e089149af991a645')
package() {
  install -D -m 444 "$srcdir/gerrit.war" "$pkgdir/usr/share/java/gerrit/gerrit.war"
  install -D -m 644 "$srcdir/gerrit.systemd" "$pkgdir/usr/lib/systemd/system/gerrit.service"
  install -D -m 644 "$srcdir/gerrit.conf" "$pkgdir/etc/default/gerritcodereview"
  install -m 755 -d "$pkgdir/var/lib/gerrit"
}

# vim:set ts=2 sw=2 et:

