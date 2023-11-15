pkgname=archx-terminal
pkgver=1.01
pkgrel=1
pkgdesc="Bspwm Configurations for ArchX"
arch=('any')
url="https://github.com/archcraft-os/archcraft-bspwm"
license=('GPL3')
depends=(
  'kitty' 'ttf-fira-code' 'ttf-firacode-nerd'
)
install="${pkgname}.install"
options=(!strip !emptydirs)

prepare() {
  cp -af ../files/. "$srcdir"
}

package() {
  local _skeldir="$pkgdir"/etc/skel
	local _configdir="$_skeldir"/.config
  local _ktdir="$_configdir"/kitty

  mkdir -p "$_skeldir" && mkdir -p "$_configdir"
  echo $srcdir
  echo $_configdir
  cp -r "$srcdir"/* "$_configdir"
}
