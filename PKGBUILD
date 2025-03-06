# Maintainer: Veillain <veillainwertz@gmail.com>
pkgname=dotman
pkgver=0.1.0.r1.g68a7dee
pkgrel=1
pkgdesc="Surprisingly a very simple DOTfile MANager, fully created using bash."
arch=('any')
url="https://github.com/veillain/dotman"
license=('GPL3')
depends=('git')
makedepends=('git' 'systemd')
provides=("dotman=${pkgver%%.r*}")
conflicts=('dotman')
source=("${pkgname}-${pkgver}::git+https://github.com/veillain/dotman.git")
sha256sums=('SKIP')

pkgver() {
    cd "$pkgname-$pkgver"
    git describe --long --tags --abbrev=7 | sed 's/\([^-]*-g\)/r\1/;s/-/./g'
}

build() {
	cd "$pkgname-$pkgver"
    sudo rm -rf usr/bin/dotman
}

package() {
	cd "$pkgname-$pkgver"
    sudo cp -rf src/dotman /usr/bin/
}
