# Maintainer: Christophe LAVIE <christophe.lavie@laposte.net>
pkgname='gnome-mojave-timed-wallpaper-rs'
_gitname='gnome-mojave-timed-wallpaper'
pkgver=1
pkgrel=1
arch=('any')
url="https://github.com/japamax/${_gitname}"
pkgdesc="GNOME time based Mojave wallpaper real scheludes"
depends=(gnome-shell gnome-backgrounds)
conflicts=('gnome-mojave-timed-wallpaper')
source=("git+https://github.com/japamax/${_gitname}")
sha256sums=('SKIP')

pkgver() {
  cd $_gitname
  git describe --tags --long | sed -r 's/^v//;s/([^-]*-g)/r\1/;s/-/./g'
}

package() {
  cd $_gitname
	install -Dm644 "${srcdir}/mojave" "${pkgdir}/usr/share/backgrounds/gnome"
	install -Dm644 "${srcdir}/mojave-timed.xml" "${pkgdir}/usr/share/backgrounds/gnome"
	install -Dm644 "${srcdir}/mojave.xml" "${pkgdir}/usr/share/gnome-background-properties"
}
