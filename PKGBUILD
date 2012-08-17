# Maintainer: Marcel Huber <marcelhuberfoo at gmail dott com>

pkgname=gerrit
pkgver=2.4.2
pkgrel=1
epoch=
pkgdesc="A web-based code review tool built on top of the git version control system"
arch=(any)
url="http://code.google.com/p/gerrit/"
license=('Apache')
groups=()
depends=(java-runtime)
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=(etc/conf.d/gerrit etc/logrotate.d/gerrit)
options=()
install=gerrit.install
changelog=changelog
source=(gerrit.war::http://gerrit.googlecode.com/files/gerrit-$pkgver.war
        gerrit.conf
        gerrit.rcd
        gerrit.systemd
        logrotate)
noextract=(gerrit.war)
sha256sums=()
package() {
  install -D -m 444 "$srcdir/gerrit.war" "$pkgdir/usr/share/java/gerrit/gerrit.war"
  install -D -m 755 "$srcdir/gerrit.rcd" "$pkgdir/etc/rc.d/gerrit"
  install -D -m 644 "$srcdir/gerrit.systemd" "$pkgdir/etc/systemd/system/gerrit.service"
  install -D -m 644 "$srcdir/gerrit.conf" "$pkgdir/etc/default/gerritcodereview"
  install -D -m 644 "$srcdir/logrotate" "${pkgdir}/etc/logrotate.d/gerrit"
  install -m 755 -d "$pkgdir/var/log/gerrit"
  install -m 755 -d "$pkgdir/var/lib/gerrit"
  install -m 755 -d "$pkgdir/var/cache/gerrit/war"
}

# vim:set ts=2 sw=2 et:

