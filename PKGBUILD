pkgname=android-udev-rules
pkgver=20230303
pkgrel=1
pkgdesc="These rules refer to Run Apps on a Hardware Device - Android Studio" 
arch=('any')
url="https://github.com/M0Rf30/android-udev-rules"
license=('GPL3')
install=android-udev-rules.install
source=("https://github.com/M0Rf30/android-udev-rules/archive/refs/tags/$pkgver.tar.gz")
md5sums=('fb17ab903d732a928526b9bed6c91462')

package() {
    cd "$srcdir/$pkgname-$pkgver"
    install -dm755 "${pkgdir}/etc/udev/rules.d/"
    install -Dm644 "51-android.rules" "${pkgdir}/etc/udev/rules.d/"
    install -dm755 "${pkgdir}/usr/lib/sysusers.d/"
    install -Dm644 "android-udev.conf" "${pkgdir}/usr/lib/sysusers.d/"
}

