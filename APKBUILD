pkgname=firmware-samsung-j5xlte
pkgver=1
pkgrel=0
pkgdesc="Firmware for Samsung Galaxy J5 (2016) (SM-J510FN)"
url="https://github.com/Kiciuk/SM-J510-Firmware/raw/master/SM-J510FN.tar.xz"
subpackages="$pkgname-venus $pkgname-wcnss"
arch="aarch64"
license="proprietary"
options="!check !strip !archcheck"
source="https://github.com/Kiciuk/SM-J510-Firmware/raw/master/SM-J510FN.tar.xz"

_fwdir="/lib/firmware/postmarketos"

package() {
	# parent package is empty
	mkdir -p "$pkgdir"
}

venus() {
	pkgdesc="Samsung Galaxy J5 (2016) (SM-J510FN) video firmware"
	install -Dm644 "$srcdir"/venus.* -t "$subpkgdir/$_fwdir"/qcom/venus-1.8
}

wcnss() {
	pkgdesc="Samsung Galaxy J5 (2016) (SM-J510FN) WiFi/BT firmware"
	cd "$srcdir"
	install -Dm644 wcnss.* -t "$subpkgdir/$_fwdir"
	install -Dm644 WCNSS_* -t "$subpkgdir/$_fwdir"/wlan/prima
}



