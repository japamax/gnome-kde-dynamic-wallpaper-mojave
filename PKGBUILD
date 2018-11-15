# Maintainer: Christophe LAVIE <christophe.lavie@laposte.net>
pkgname='gnome-mojave-timed-wallpaper-rs'
_gitname='gnome-mojave-timed-wallpaper'
pkgver=1
pkgrel=1
arch=('any')
url="https://github.com/japamax/${_gitname}"
pkgdesc="GNOME time based Mojave wallpaper real scheludes"
depends=(gnome-shell gnome-backgrounds)
conflicts=('gnome-mojave-timed-wallpaper' 'gnome-theme-macos-mojave-meta')
source=("git+https://github.com/japamax/${_gitname}")
sha256sums=('SKIP')

pkgver() {
  cd ${_gitname}"
  git describe --tags --long | sed -r 's/^v//;s/([^-]*-g)/r\1/;s/-/./g'
}

package() {
  cd "${srcdir}/${_gitname}"
  install -dm755 "${pkgdir}/usr/share/backgrounds/gnome/mojave"
  install -m644 ${srcdir}/${_gitname}/mojave/* "${pkgdir}/usr/share/backgrounds/gnome/mojave"
  install -Dm644 mojave-timed.xml "${pkgdir}/usr/share/backgrounds/gnome/mojave-timed.xml"
  install -Dm644 mojave.xml "${pkgdir}/usr/share/gnome-background-properties/mojave.xml"
 }
