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
backup=(etc/default/gerritcodereview)
options=()
install=gerrit.install
changelog=changelog
source=(gerrit.war::http://gerrit.googlecode.com/files/gerrit-$pkgver.war
        gerrit.conf
        gerrit.rcd
        gerrit.systemd)
noextract=(gerrit.war)
sha256sums=("70342c53969c898211b43de0856ecf8d6d658174e718d4beda5348158995398f" "246561b39f25db54d749d9d87503835f0cf6c29fc1c88edc62a8412bd6c308a6" "de5d4e58ba810626a84b2aaf4e2602ad01260b69b476be294dba2d36ab55e324" "be1d205c6a0f3b24aad3c385f8188c64bfa3a9799ecf8ce5e089149af991a645")
package() {
  install -D -m 444 "$srcdir/gerrit.war" "$pkgdir/usr/share/java/gerrit/gerrit.war"
  install -D -m 755 "$srcdir/gerrit.rcd" "$pkgdir/etc/rc.d/gerrit"
  install -D -m 644 "$srcdir/gerrit.systemd" "$pkgdir/etc/systemd/system/gerrit.service"
  install -D -m 644 "$srcdir/gerrit.conf" "$pkgdir/etc/default/gerritcodereview"
  install -m 755 -d "$pkgdir/var/lib/gerrit"
  install -m 755 -d "$pkgdir/srv/gerrit-review"
}

# vim:set ts=2 sw=2 et:

