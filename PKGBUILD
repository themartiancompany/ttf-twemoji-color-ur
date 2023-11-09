# Maintainer: zoorat <zoorat [at] protonmail [dot] com>
# Old Maintainer: Thomas Wood <grand.edgemaster@gmail.com>

pkgname=ttf-twemoji-color
pkgver=14.0.2
pkgrel=1

pkgdesc="A color and B&W emoji SVG-in-OpenType font by Twitter with support for ZWJ, skin tone modifiers and country flags."
arch=('any')
url="https://github.com/eosrei/twemoji-color-font"
license=('custom:CCPL:by-4.0' 'MIT')

depends=('fontconfig')
optdepends=('ttf-bitstream-vera: default fallback font used for configuration')
replaces=('twemoji-color-font')
conflicts=('twemoji-color-font')
provides=('twemoji-color-font' 'emoji-font')

source=("${url}/releases/download/v${pkgver}/TwitterColorEmoji-SVGinOT-Linux-${pkgver}.tar.gz")
b2sums=('43a4c3207cff2e8419c6fb7c0e5bcbe860a607757bc5a1d67c2cd49717eaf6fb259326a4a09b9bfb81b201b9f1ee97be2c3c39649a2d123a62333c7ff8c64241')

install=$pkgname.install

package() {
	cd TwitterColorEmoji-SVGinOT-Linux-${pkgver}
	install -Dm644 TwitterColorEmoji-SVGinOT.ttf -t "$pkgdir"/usr/share/fonts/twemoji-color-font/
	install -Dm644 LICENSE* -t "$pkgdir"/usr/share/licenses/$pkgname/
	install -Dm644 README.md "$pkgdir"/usr/share/doc/$pkgname/README
	install -Dm644 fontconfig/46-twemoji-color.conf "$pkgdir"/usr/share/fontconfig/conf.avail/46-$pkgname.conf
}
