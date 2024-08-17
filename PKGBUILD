# Maintainer: ant <ant@national.shitposting.agency>
# Adapted-from: Philip Goto <philip.goto@gmail.com>

pkgname=gnome-backgrounds
pkgver=46.0.0
pkgrel=2
pkgdesc='Background images and data for the Odysen Desktop'
url=https://github.com/odysen/${pkgname}
arch=(any)
depends=(webp-pixbuf-loader)
makedepends=(git glib2 meson)
provides=(gnome-backgrounds)
conflicts=(${pkgname}-git)
license=(CCPL:by-sa)
source=(git+${url})
b2sums=('SKIP')

build() {
	arch-meson ${pkgname} build
	meson compile -C build
}

check() {
	meson test -C build --print-errorlogs
}

package() {
	meson install -C build --destdir "${pkgdir}"
}
