# Contributor: Sasha Gerrand <alpine-pkgs@sgerrand.com>
# Maintainer: Sasha Gerrand <alpine-pkgs@sgerrand.com>
pkgname=git-crypt
pkgver=0.6.0
pkgrel=0
pkgdesc="Transparent file encryption in git"
url="https://www.agwa.name/projects/git-crypt/"
arch="all"
license="X11"
depends="git libgcc libstdc++ openssl"
depends_dev="openssl-dev"
makedepends="$depends_dev docbook-xsl libxslt make"
install=""
subpackages="$pkgname-dev $pkgname-doc"
source="https://www.agwa.name/projects/$pkgname/downloads/$pkgname-$pkgver.tar.gz"
builddir="$srcdir/$pkgname-$pkgver"

build() {
	cd "$builddir"
	make ENABLE_MAN=yes DOCBOOK_XSL=/usr/share/xml/docbook/xsl-stylesheets-1.79.1/manpages/docbook.xsl || return 1
}

package() {
	cd "$builddir"
	make PREFIX="$pkgdir" install || return 1
}

dev() {
	mkdir -p "$subpkgdir"
	default_dev
}

doc() {
	mkdir -p "$subpkgdir"
	default_doc
}

sha512sums="e72c57a8e3168fcdb68cde352a6ab0e397675916dfa1e4266a852e21bcbda313f9c9a58a7d6a827f33fe549f09afbb8008509a6bf1859d6804cf36ffab5c758d  git-crypt-0.6.0.tar.gz"
