# Maintainer: Alfonso Saavedra "Son Link" <sonlink.dourden@gmail.com>
pkgname=retroblazer
pkgver=0.2
pkgrel=1
pkgdesc="A FPS retro game"
arch=('i686' 'x86_64')
license=('GPL')
url="http://www.retroblazer.com"
depends=('darkplaces')
source=('http://www.retroblazer.com/RB_a0.2.zip' 'retroblazer.desktop'
	'retroblazer' 'retroblazer.png')
md5sums=('d2faae15626ab413b81e78860eb1efec'
         '3c6a84343b6cb1e43fb61b9dcac2613e'
         '36cd41a5bdfcd6690f460abd372669fd'
         'c4fa6df5acd536d0f9b8ea62e39d4302')

install=retroblazer.install
package() {
  cd "${srcdir}"

  mkdir -p $pkgdir/usr/share/$pkgname/id1
  mkdir -p $pkgdir/usr/bin
  mkdir -p $pkgdir/usr/share/pixmaps

  install -m755 ${pkgname} $pkgdir/usr/bin/$pkgname

  cp RetroBlazer/* $pkgdir/usr/share/$pkgname/id1
  
  mkdir -p $pkgdir/usr/share/applications/
  install -Dm644 "${srcdir}/${pkgname}.desktop" "${pkgdir}/usr/share/applications/"
  install -Dm644 "${srcdir}/${pkgname}.png" "${pkgdir}/usr/share/pixmaps/"
}
