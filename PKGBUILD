
pkgname=gtksourceview3
pkgver=3.18.1
_pkgver=3.18
pkgrel=1
pkgdesc="A text widget that extends the standard GTK+ text widget"
arch=('x86_64')
url="https://git.gnome.org/browse/gtksourceview/tree/README"
license=('GPL')
depends=('gtk3' 'libxml2')
makedepends=('intltool' 'gobject-introspection' 'vala')
source=("http://ftp.gnome.org/pub/gnome/sources/gtksourceview/${_pkgver}/gtksourceview-${pkgver}.tar.xz")
md5sums=('b7600b6cc06ec96ce1d028bf7a44d14b')

build() {
  cd gtksourceview-${pkgver}
  
  ./configure --prefix=/usr \
    --sysconfdir=/etc \
    --localstatedir=/var \
    --disable-static
  make
}

package() {
  cd gtksourceview-${pkgver}
  
  make DESTDIR="${pkgdir}" install
}
