pkgname=android-udev-rules
pkgver=20240221
pkgrel=1
pkgdesc='These UDEV files allow to communicate between PC and Android devices without the necessity of Administrator privileges.'
arch=('x86_64')
url='https://github.com/M0Rf30/android-udev-rules'
license=('GPL3')
depends=('systemd' 'libmtp')
install='android-udev-rules.install'
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/M0Rf30/${pkgname}/archive/${pkgver}.tar.gz")
sha1sums=('SKIP')

package() {
    install -Dm 644 "${srcdir}/${pkgname}-${pkgver}/51-android.rules" -t "${pkgdir}/usr/lib/udev/rules.d/"
    install -Dm 644 "${srcdir}/${pkgname}-${pkgver}/android-udev.conf" -t "${pkgdir}/usr/lib/sysusers.d/"

    msg2 "Post installaction script will add current USER *$USER* to *adbusers* GROUP.
    Please see the output of */etc/group*

`cat /etc/group`

for correction . . .
"
}
