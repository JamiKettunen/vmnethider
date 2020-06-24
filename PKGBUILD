_gitname="vmnethider"
_pkgname="gnome-shell-extension-$_gitname"
pkgname="$_pkgname-git"
pkgdesc="GNOME Extension to hide the vmnet Interfaces"
pkgver=r9.40e98f4
pkgrel=1
arch=("any")
url="https://github.com/JamiKettunen/$_gitname"
license=("GPL3")
depends=("gnome-shell>=3.36" "networkmanager")
makedepends=("git")
provides=("$_pkgname")
source=("git://github.com/JamiKettunen/$_gitname.git")
md5sums=("SKIP")

pkgver() {
	cd "$_gitname"

	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
	cd "$_gitname"

	mkdir -p "$pkgdir"/usr/share/gnome-shell/extensions/vmnethider@t0by.eu/
	install -Dm644 {extension.js,metadata.json} "$pkgdir"/usr/share/gnome-shell/extensions/vmnethider@t0by.eu/
	install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$_pkgname/COPYING
}
