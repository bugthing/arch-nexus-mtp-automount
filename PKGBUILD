# Maintainer: Benjamin Martin <benjamin247365@hotmail.com>
pkgname=android-mtp
pkgver=0.5
pkgrel=1
pkgdesc="Adds udev rules to automount Android devices (using go-mtpfs-git)"
arch=('any')
url="https://github.com/bugthing/arch-nexus-mtp-automount"
license=('unknown')
depends=(go-mtpfs-git)
source=('99-android-mtp.rules' 'android-mtp@.service')
md5sums=('ff01a763e8542be576f9c1f31e5b4bc6'
'6a371ca3357f4a1c2887f1a639180813')
install='android-mtp.install'

package() {
  mkdir -p $pkgdir/usr/lib/udev/rules.d/
  mkdir -p $pkgdir/usr/lib/systemd/system/
  cp $srcdir/99-android-mtp.rules $pkgdir/usr/lib/udev/rules.d/99-android-mtp.rules
  cp $srcdir/android-mtp@.service $pkgdir/usr/lib/systemd/system/android-mtp@.service
  chmod a+r $pkgdir/usr/lib/udev/rules.d/99-android-mtp.rules
  chmod a+r $pkgdir/usr/lib/systemd/system/android-mtp@.service
}

# vim:set ts=2 sw=2 et:
