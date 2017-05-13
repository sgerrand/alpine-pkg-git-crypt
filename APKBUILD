# Contributor: Sasha Gerrand <alpine-pkgs@sgerrand.com>
# Maintainer: Sasha Gerrand <alpine-pkgs@sgerrand.com>
pkgname=git-crypt
pkgver=0.5.0
pkgrel=0
pkgdesc="Transparent file encryption in git"
url="https://www.agwa.name/projects/git-crypt/"
arch="all"
license="X11"
depends="git openssl"
depends_dev="openssl-dev"
makedepends="$depends_dev libxslt make"
install=""
subpackages="$pkgname-dev $pkgname-doc"
source="https://www.agwa.name/projects/$pkgname/downloads/$pkgname-$pkgver.tar.gz"
builddir="$srcdir/$pkgname-$pkgver"

build() {
	cd "$builddir"
	make ENABLE_MAN=yes || return 1
}

package() {
	cd "$builddir"
	make ENABLE_MAN=yes PREFIX="$pkgdir" install || return 1
}

dev() {
	mkdir -p "$subpkgdir"
	default_dev
}

doc() {
	mkdir -p "$subpkgdir"
	default_doc
}

md5sums="a7c6149606e492ba7dc9fe4658482ac7  git-crypt-0.5.0.tar.gz"
sha256sums="0a8f92c0a0a125bf768d0c054d947ca4e4b8d6556454b0e7e87fb907ee17cf06  git-crypt-0.5.0.tar.gz"
sha512sums="c728bc210047d563b6a4ddc3b3336afb08c25b75aa906237f38b71651169d33bf40001c45f8af8287d539592104b48a5a8f6f330541c5cbafa992d328048fe0c  git-crypt-0.5.0.tar.gz"
