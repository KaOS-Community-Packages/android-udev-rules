pkgname=android-udev-rules
pkgver=20231104
pkgrel=1
pkgdesc="These files allow to communicate between PC and Android devices" 
arch=('any')
url="https://github.com/M0Rf30/android-udev-rules"
license=('GPL3')
source=("${pkgname}-${pkgver}.zip::https://github.com/M0Rf30/android-udev-rules/archive/refs/tags/${pkgver}.tar.gz")
md5sums=('fb184c737bd064e23f8209da6ed19d9e')

package() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    install -dm755 "${pkgdir}/etc/udev/rules.d/"
    install -Dm644 "51-android.rules" "${pkgdir}/etc/udev/rules.d/"
    install -dm755 "${pkgdir}/usr/lib/sysusers.d/"
    install -Dm644 "android-udev.conf" "${pkgdir}/usr/lib/sysusers.d/"
}
