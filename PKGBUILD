# Maintainer: Bogusław Witkowski <vibowit@vibowit.com>

pkgname=spotified-git
pkgver=0.0.1
pkgrel=1
pkgdesc="Spotify Connect client + daemon for the Raspberry Pi, based off librespot."
arch=('armv7h')
url="https://github.com/vibowit/spotified"
license=('MIT')
groups=('spotified')
depends=('alsa-lib' 'gcc-libs')
install='spotified.install'
# source=("https://github.com/dtcooper/raspotify/releases/download/0.11.3/raspotify_0.11.3.librespot.20180517T232041Z.431be9e_armhf.deb")
# md5sums=('6ae6b1914404a586b0e46206664eb515')

package() {
	install -d "${pkgdir}/usr/bin"
	install -d "${pkgdir}/etc/default"
	install -d "${pkgdir}/usr/lib/systemd/system"
	install -d "${pkgdir}/usr/share/licenses/${pkgname}"

	install -m644 "${srcdir}/etc/default/spotified" "${pkgdir}/etc/default"
	install -m644 "${srcdir}/usr/share/doc/spotified/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}"
	install -m755 "${srcdir}/usr/bin/librespot" "${pkgdir}/usr/bin"
	install -m644 "${srcdir}/usr/lib/systemd/system/spotified.service" "${pkgdir}/usr/lib/systemd/system"
}
