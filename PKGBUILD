# Maintainer: Robert Fry <contact@robertfry.xyz>

pkgname=nightpdf
pkgver=0.4.0
pkgrel=1
pkgdesc='Dark mode PDF reader'
arch=('x86_64')
url='https://github.com/Lunarequest/NightPDF'
license=('GPLv2')
depends=()
makedepends=()
provides=('nightpdf')
conflicts=('nightpdf')
source=('https://github.com/Lunarequest/NightPDF/releases/download/v0.4.0/NightPDF_0.4.0_amd64.deb'
        'patch.patch')
sha256sums=('08e7dc2c4c0e2494049b6c775e7b79729b6fa736907922ee9f21b2a64c52e8ee'
            'SKIP')

package() {
    ar x NightPDF_0.4.0_amd64.deb
    tar -xf data.tar.xz --directory "${pkgdir}"
    patch --directory="${pkgdir}" --strip=0 --forward --input="${srcdir}/patch.patch"
}
