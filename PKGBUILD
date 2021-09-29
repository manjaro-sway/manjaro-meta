# Maintainer: Stefano Capitani <stefano@manjaro.org>
# Maintainer: Philip Müller <philm@manjaro.org>
# Maintainer: Roland Singer <roland@manjaro.org>
# Contributor: Shrinivas Kumbhar (aka Librewish)
pkgname=('manjaro-alsa'
         'manjaro-bluetooth'
         'manjaro-connman'
         'manjaro-gstreamer'
         'manjaro-input'
         'manjaro-modem'
         'manjaro-pipewire'
         'manjaro-pulse'
         )
pkgbase=manjaro-meta
pkgver=20210928
pkgrel=1
arch=('any')
url="www.manjaro.org"
license=('GPL')
source=('realtime-privileges.sh'
        'realtime-privileges.hook')
sha256sums=('de4521b2e801bb5ba53bddfaa5e62a8ebd3c7ff8247a1269f9f3b0e9821e6a46'
            '964d6e10a3af9d6dbe1d87ac0ca0b775e98cfe4719010b6efec6e812318cfc5a')

pkgver() {
  date +%Y%m%d
}

package_manjaro-alsa() {
  pkgdesc="Manjaro meta package for complete ALSA support"
  depends=('alsa-firmware'
           'alsa-lib'
           'alsa-oss'
           'alsa-plugins'
           'alsa-utils')
  optdepends=('alsa-tools')
}

package_manjaro-bluetooth() {
  pkgdesc="Manjaro meta package for complete Bluetooth support"
  depends=('bluez'
           'bluez-cups'
           'bluez-hid2hci'
           'bluez-libs'
           'bluez-plugins'
           'bluez-tools'
           'bluez-utils'
           'pulseaudio-bluetooth')
  optdepends=('blueberry: Bluetooth configuration tool'
              'bluedevil: Qt Bluetooth frontend'
              'blueman: A Gtk+ Bluetooth manager')
}

package_manjaro-connman() {
  pkgdesc="Manjaro meta package for complete ConnMan support"
  depends=('avahi'
           'connman'
           'dnsmasq'
           'nss-mdns'
           'ofono'
           'openconnect'
           'openresolv'
           'openssh'
           'openvpn'
           'ntp'
           'pacrunner'
           'pptpclient'
           'rp-pppoe'
           'wpa_supplicant')
  optdepends=('cmst: A Qt GUI for connman'
              'connman-gtk: A GTK GUI for connman'
              'gufw: Uncomplicated firewall GTK GUI'
              'manjaro-settings-samba: Preconfigured samba settings'
              'nx-firewall: kcm module for firewall')
}

package_manjaro-gstreamer() {
  pkgdesc="Manjaro meta package for complete Gstreamer support"
  depends=('ffmpeg'
           'gst-libav'
           'gst-plugins-bad'
           'gst-plugins-base'
           'gst-plugins-good'
           'gst-plugins-ugly')
}

package_manjaro-input() {
  pkgdesc="Manjaro meta package for complete input support"
  depends=('xf86-input-elographics'
           'xf86-input-evdev'
           'xf86-input-libinput'
           'xf86-input-void'
           'xf86-input-wacom')
optdepends=('gestures: Gtk+ GUI for touchpad gestures'
            'touche: Qt GUI for touchpad gestures')
}

package_manjaro-modem() {
  pkgdesc="Manjaro meta package for complete modem support"
  depends=('modemmanager'
           'mobile-broadband-provider-info'
           'usb_modeswitch')
  optdepends=('gpsd: GPS daemon and library to support USB/serial GPS devices'
              'modem-manager-gui: A gui for modem manager')
}

package_manjaro-pipewire() {
  pkgdesc="Manjaro meta package for complete PipeWire support."
  depends=('gst-plugin-pipewire'
           'pipewire'
           'pipewire-alsa'
           'pipewire-jack'
           'pipewire-pulse'
           'pipewire-zeroconf'
           'sof-firmware')
  optdepends=('realtime-privileges: Realtime privileges for users'
              'wireplumber: Alternative session / policy manager implementation')
  conflicts=('manjaro-pulse'
             'pulseaudio-equalizer'
             'pulseaudio-jack'
             'pulseaudio-lirc'
             'pulseaudio-rtp'
             'pulseaudio-zeroconf')

  install -Dm644 realtime-privileges.hook -t "$pkgdir"/usr/share/libalpm/hooks/
  install -Dm755 realtime-privileges.sh "$pkgdir"/usr/bin/realtime-privileges
}

package_manjaro-pulse() {
  pkgdesc="Manjaro meta package for complete PulseAudio support"
  depends=('pulseaudio'
           'pulseaudio-alsa'
           'pulseaudio-bluetooth'
           'pulseaudio-jack'
           'pulseaudio-lirc'
           'pulseaudio-rtp'
           'pulseaudio-zeroconf'
           'sof-firmware')
  optdepends=('paprefs: Configuration dialog'
              'pasystray: system tray application'
              'pavucontrol: A GTK volume control tool'
              'pavucontrol-qt: A Qt volume control tool'
              'pulseaudio-ctl: Control volume from the shell or mapped to keyboard shortcuts'
              'pulseaudio-equalizer: for equalizer sink (qpaeq)'
              'pulseaudio-equalizer-ladspa: A GUI equalizer')
  conflicts=('lib32-pipewire-jack'
             'manjaro-pipewire'
             'pipewire-jack'
             'pipewire-pulse'
             'pipewire-zeroconf')
}
