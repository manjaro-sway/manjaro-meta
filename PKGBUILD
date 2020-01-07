# Maintainer: Stefano Capitani <stefano@manjaro.org>
# Maintainer: Philip Müller <philm@manjaro.org>
# Maintainer: Roland Singer <roland@manjaro.org>

pkgbase=manjaro-meta
arch=('i686' 'x86_64')
pkgname=('manjaro-alsa'
	 'manjaro-pulse'
         'manjaro-gstreamer'
         'manjaro-vaapi'
         'manjaro-network'
         'manjaro-modem'
         'manjaro-bluetooth'
         'manjaro-printer'
)

pkgver=20200107
pkgrel=1
url="www.manjaro.org"
license=('GPL')

pkgver() {

    date +%Y%m%d
}

package_manjaro-alsa() {
	pkgdesc="manjaro ALSA support (Meta-PKG)"
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
	pkgdesc="manjaro Pulseaudio support (Meta-PKG)"
	if [ "$CARCH" = "i686" ]; then
		depends=("pulseaudio" 
			"pulseaudio-alsa")
	elif [ "$CARCH" = "x86_64" ]; then
		depends=("pulseaudio"
			"pulseaudio-alsa"
                        "pulseaudio-ctl"
                        "pulseaudio-jack"
                        "pulseaudio-zeroconf"
                        "pulseaudio-lirc"
                        "fluidsynth"
                        "openal"
                        "libcanberra-gstreamer"
                        "lib32-openal"
                        "lib32-fluidsynth"
                        "lib32-libcanberra-gstreamer"
			"lib32-libcanberra-pulse"
			"lib32-libpulse")
	fi
	optdepends=('pavucontrol: A GTK volume control tool for PulseAudio'
                        'pulseaudio-equalizer-ladspa: A gui equalizer for pulseaudio'
                        'pasystray: pulseaudio system tray'
                        'paprefs: configuration dialog for pulseaudio')
}

package_manjaro-gstreamer() {
	pkgdesc="manjaro gstreamer support (Meta-PKG)"
		depends=("ffmpeg"
                        "gst-libav"
                        "gst-plugins-bad"
                        "gst-plugins-base"
                        "gst-plugins-good"
                        "gst-plugins-ugly"
                        "gst-plugins-espeak")
}

package_manjaro-vaapi() {
	pkgdesc="manjaro VA-API support (Meta-PKG)"
		depends=("libva-intel-driver"
                        "libva-mesa-driver"
                        "libva-vdpau-driver"
                        "lib32-libva-intel-driver"
                        "lib32-libva-mesa-driver"
                        "lib32-libva-vdpau-driver")
}

package_manjaro-network() {
	pkgdesc="manjaro network support (Meta-PKG)"
		depends=("networkmanager"
                        "networkmanager-openconnect"
                        "networkmanager-openvpn"
                        "networkmanager-pptp"
                        "networkmanager-vpnc"
                        "networkmanager-strongswan"
                        "network-manager-sstp"
                        "networkmanager-fortisslvpn"
                        "networkmanager-dispatcher-sshd"
                        "networkmanager-dispatcher-ntpd"
                        "rp-pppoe"
                        "openresolv"
                        "openssh"
                        "avahi"
                        "nss-mdns"
                        "dnsmasq"
                        "wpa_supplicant")
	optdepends=('network-manager-applet: Applet for managing network connection'
                        'firewalld: Firewall daemon with D-Bus interface')
}

package_manjaro-modem() {
	pkgdesc="manjaro modem support (Meta-PKG)"
		depends=("modemmanager"
                        "mobile-broadband-provider-info"
                        "usb_modeswitch")
	optdepends=('modem-manager-gui: A gui for modem manager')
}

package_manjaro-bluetooth() {
	pkgdesc="manjaro bluetooth support (Meta-PKG)"
		depends=("bluez"
                        "bluez-libs"
                        "bluez-cups"
                        "bluez-hid2hci"
                        "bluez-plugins"
                        "bluez-tools"
                        "bluez-utils"
                        "pulseaudio-bluetooth")
	optdepends=('blueman: A gtk+ bluetooth manager'
                        'bluedevil: qt bluetooth frontend'
                        'blueberry: bluetooth configuration tool')
}

package_manjaro-printer() {
	pkgdesc="manjaro printer support (Meta-PKG)"
		depends=("cups"
                        "cups-pdf"
                        "cups-pk-helper"
                        "ghostscript"
                        "gsfonts"
                        "gutenprint"
                        "hplip"
                        "python-gobject"
                        "python-pyqt5"
                        "python-pysmbc"
                        "splix"
                        "system-config-printer"
                        "colord-sane")
	optdepends=('print-manager: A kde tool for managing print jobs and printers'
                        'xsane: gtk2 frontend for scanner'
                        'simple-scan: gtk3 frontend for scanner'
                        'skanlite: Image Scanning Application for KDE')
}

