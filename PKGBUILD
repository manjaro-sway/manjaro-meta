# Maintainer: Stefano Capitani <stefano@manjaro.org>
# Maintainer: Philip Müller <philm@manjaro.org>
# Maintainer: Roland Singer <roland@manjaro.org>
# Contributor: Shrinivas Kumbhar (aka Librewish) <Librewisk@forum.manjaro.org>
pkgbase=manjaro-meta
arch=('i686' 'x86_64')
pkgname=('manjaro-alsa'
	 'manjaro-pulse'
         'manjaro-gstreamer'
         'manjaro-vaapi'
         'manjaro-network'
         'manjaro-connman'
         'manjaro-modem'
         'manjaro-bluetooth'
         'manjaro-printer'
         'manjaro-input'
)

pkgver=20200126
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
			"alsa-lib"
                        "alsa-plugins"
                        "alsa-oss")
	elif [ "$CARCH" = "x86_64" ]; then
		depends=("alsa-utils"
			"alsa-firmware"
			"alsa-lib"
                        "alsa-plugins"
                        "alsa-oss"
			"lib32-alsa-lib"
                        "lib32-alsa-oss"
			"lib32-alsa-plugins")
	fi
	optdepends=('alsa-tools')
}

package_manjaro-pulse() {
	pkgdesc="manjaro Pulseaudio support (Meta-PKG)"
	if [ "$CARCH" = "i686" ]; then
		depends=("pulseaudio" 
			"pulseaudio-alsa")
	elif [ "$CARCH" = "x86_64" ]; then
		depends=("pulseaudio"
			"pulseaudio-alsa"
                        "pulseaudio-equalizer"
                        "pulseaudio-jack"
                        "pulseaudio-zeroconf"
                        "pulseaudio-lirc"
                        "fluidsynth"
                        "openal"
                        "libcanberra-gstreamer"
                        "libcanberra-pulse"
                        "lib32-openal"
                        "lib32-fluidsynth"
                        "lib32-libcanberra-gstreamer"
			"lib32-libcanberra-pulse"
			"lib32-libpulse")
	fi
	optdepends=('pavucontrol: A GTK volume control tool for PulseAudio'
                        'pulseaudio-equalizer-ladspa: A gui equalizer for pulseaudio'
                        'pasystray: pulseaudio system tray'
                        'paprefs: configuration dialog for pulseaudio'
                        'pulseaudio-ctl: Control PulseAudio volume from the shell or mapped to keyboard shortcuts')
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
                        "intel-media-driver"
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
                        "wpa_supplicant"
                        "manjaro-settings-samba")
	optdepends=('network-manager-applet: Applet for managing network connection'
                        'nm-tray: A pure QT NetworkManager front-end residing in panels'
                        'firewalld: Firewall daemon with D-Bus interface')
}

package_manjaro-connman() {
	pkgdesc="manjaro connman support (Meta-PKG)"
		depends=("connman"
                        "ofono"
                        "pacrunner"
                        "wpa_supplicant"
                        "rp-pppoe"
                        "openresolv"
                        "openssh"
                        "openconnect"
                        "openvpn"
                        "pptpclient"
                        "avahi"
                        "nss-mdns"
                        "dnsmasq"
                        "ntp"
                        "manjaro-settings-samba")
	optdepends=('cmst: A QT gui for connman'
                        'connman-gtk: a GTK gui for connman'
                        'qomui: A QT gui for vpn management'
                        'gufw: a GTK gui for Uncomplicated firewall'
                        'nx-firewall: kcm module for firewall')
}

package_manjaro-modem() {
	pkgdesc="manjaro modem support (Meta-PKG)"
		depends=("modemmanager"
                        "mobile-broadband-provider-info"
                        "usb_modeswitch")
	optdepends=('modem-manager-gui: A gui for modem manager'
                        'gpsd: GPS daemon and library to support USB/serial GPS devices')
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
                        "foomatic-db"
                        "foomatic-db-gutenprint-ppds"
                        "python-gobject"
                        "python-pyqt5"
                        "python-pysmbc"
                        "python-reportlab"
                        "splix"
                        "colord-sane")
	optdepends=('system-config-printer: A gtk cups printer configuration tool and status applet'
                        'print-manager: A kde tool for managing print jobs and printers'
                        'xsane: gtk2 frontend for scanner'
                        'simple-scan: gtk3 frontend for scanner'
                        'skanlite: Image Scanning Application for KDE')
}

 package_manjaro-input() {
	pkgdesc="manjaro input support (Meta-PKG)"
		depends=("xf86-input-elographics"
                        "xf86-input-evdev"
                        "xf86-input-void"
                        "xf86-input-libinput"
                        "xf86-input-wacom"
                        "libinput-gestures"
                        "iio-sensor-proxy"
                        "fprintd"
                        "bolt")
	optdepends=('gestures: a minimal gtk+ gui for libinput-gesture'
                        'easystroke: control your desktop using mouse gesture'
                        'piper: GTK application to configure gaming mice'
                        'fancontrol-gui: Gui for fancontrol'
                        'fingerprint-gui: Application for fingerprint-based authentication, automatically support UPEK fingerprint readers with non-free library'
                        'plasma-thunderbolt: plasma integration for managing thunderbolt devices')
}



