# Maintainer: BanHammer  <no@e.mail>

pkgname="holo-bin"
pkgver=0.3.0
pkgrel=1
pkgdesc="A terminal UI for Android developers. Monitor performance, browse logs, query databases, record traces, and control devices — without leaving the terminal."
arch=('x86_64')
url="https://github.com/measure-sh/holo"
license=('MIT')
depends=("android-tools")
optdepends=(
    "scrcpy: required for device mirroring"
)
options=(!strip !debug)
source_x86_64=("${pkgname}-${pkgver}.tar.gz::https://github.com/measure-sh/holo/releases/download/v${pkgver}/holo-x86_64-unknown-linux-gnu.tar.gz")
sha256sums_x86_64=("1c1a940bcac038f2ac8d63537cdfcb6366a3abaefb16602377184cb57d3926cf")

package() {
    cd ${srcdir}
    install -Dm755 "${srcdir}/holo" "${pkgdir}/opt/${pkgname}/holo"
    install -dm755 "$pkgdir/usr/bin"
    ln -s "/opt/${pkgname}/holo" "${pkgdir}/usr/bin/holo"
}
