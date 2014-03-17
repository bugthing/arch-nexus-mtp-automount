# Maintainer: Benjamin Martin <benjamin247365@hotmail.com>
pkgname=android-mtp
pkgver=0.2
pkgrel=1
pkgdesc="Adds udev rules to automount Android devices"
arch=('any')
url="https://github.com/bugthing/arch-nexus-mtp-automount"
license=('unknown')
depends=(mtpfs)
source=('99-android-mtp.rules' 'android-mtp@.service')
md5sums=('ff01a763e8542be576f9c1f31e5b4bc6'
'4b2a63952453d480f2edef72876d1dd8')
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
