# Maintainer: Your Name <your.email@example.com>
pkgname=package-name
pkgver=1.0.0
pkgrel=1
pkgdesc="A brief description of your package"
arch=('x86_64')
url="https://github.com/YourUsername/YourRepository"
license=('MIT')
depends=('bash')
optdepends=()
backup=('etc/package-name.conf')
source=("${pkgname}-${pkgver}.tar.gz::${url}/archive/refs/tags/v${pkgver}.tar.gz")
sha256sums=('SKIP')

package() {
    cd "${srcdir}/YourRepository-${pkgver}"
    
    # Install the main script
    install -Dm755 "package-name.sh" "${pkgdir}/usr/bin/${pkgname}"
    
    # Install configuration file
    install -Dm644 "package-name.conf" "${pkgdir}/etc/${pkgname}.conf"
    
    # Install systemd service
    install -Dm644 "package-name.service" "${pkgdir}/usr/lib/systemd/system/${pkgname}.service"
    
    # Install license
    install -Dm644 "LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
