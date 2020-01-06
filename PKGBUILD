# Maintainer: Philip Müller <philm@manjaro.org>
# Maintainer: Roland Singer <roland@manjaro.org>

pkgbase=manjaro-meta
arch=('i686' 'x86_64')
pkgname=('manjaro-alsa'
	 'manjaro-pulse'
)

pkgver=2015.06
pkgrel=3
url="www.manjaro.org"
license=('GPL')

package_manjaro-alsa() {
	pkgdesc="Manjaro ALSA support (Meta-PKG)"
	if [ "$CARCH" = "i686" ]; then
		depends=("alsa-utils"
			"alsa-firmware"
			"alsa-lib")
	elif [ "$CARCH" = "x86_64" ]; then
		depends=("alsa-utils"
			"alsa-firmware"
			"alsa-lib"
			"lib32-alsa-lib"
			"lib32-alsa-plugins")
	fi
	optdepends=('xfce4-mixer: The volume control plugin for the Xfce panel'
			'pnmixer: GTK volume mixer applet that runs in the system tray'
			'pnmixer-xfce4: GTK volume mixer applet that runs in the system tray')
}

package_manjaro-pulse() {
	pkgdesc="Manjaro Pulseaudio support (Meta-PKG)"
	if [ "$CARCH" = "i686" ]; then
		depends=("pulseaudio" 
			"pulseaudio-alsa")
	elif [ "$CARCH" = "x86_64" ]; then
		depends=("pulseaudio"
			"pulseaudio-alsa"
			"lib32-libcanberra-pulse"
			"lib32-libpulse")
	fi
	optdepends=('pavucontrol: A GTK volume control tool for PulseAudio'
			'pnmixer: GTK volume mixer applet that runs in the system tray'
			'pnmixer-xfce4: GTK volume mixer applet that runs in the system tray')
}

