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
         'manjaro-connman'
         'manjaro-modem'
         'manjaro-bluetooth'
         'manjaro-input'
)

pkgver=20210102
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
        		"sof-firmware"
				"pulseaudio-alsa"
        		"pulseaudio-jack"
        		"pulseaudio-zeroconf"
        		"pulseaudio-lirc"
        		"pulseaudio-rtp"
        		"pulseaudio-equalizer"
        		"pulseaudio-bluetooth")
     fi
optdepends=('pavucontrol: A GTK volume control tool for PulseAudio'
           'pavucontrol-qt: A QT volume control tool for PulseAudio'
           'pulseaudio-equalizer-ladspa: A GUI equalizer for PulseAudio'
           'pasystray: pulseaudio system tray'
           'paprefs: configuration dialog for pulseaudio'
           'pulseaudio-ctl: Control PulseAudio volume from the shell or mapped to keyboard shortcuts')
conflicts=('pipewire-support')
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




