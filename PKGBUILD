# Contributor: Luca Bennati <lucak3 AT gmail DOT com>
# Maintainer: Luca Bennati <lucak3 AT gmail DOT com>

pkgname=jpdfbookmarks
pkgver=2.5.2
pkgrel=1
_pkgreal="${pkgname}-${pkgver}"
pkgdesc="Java PDF bookmarks editor"
arch=('any')
url="http://flavianopetrocchi.blogspot.com/"
license=('GPL3')
depends=('java-environment' 'hicolor-icon-theme')
install=jpdfbookmarks.install
source=("http://downloads.sf.net/sourceforge/${pkgname}/${_pkgreal}.tar.gz"
              jpdfbookmarks.desktop)
md5sums=('035c9cb2f828891cf0bea37323968f7a'
                   '0d3d8e406fde4f9cdcb410a241a309b9')

build() {
  true
}

package() {
  cd "${srcdir}/${_pkgreal}"

  mkdir -p "${pkgdir}/usr/share/java/${pkgname}/lib/"
  install -Dm644 lib/* "${pkgdir}/usr/share/java/${pkgname}/lib/"
  install -Dm755 jpdfbookmarks.jar "${pkgdir}/usr/share/java/${pkgname}/"
  install -DTm755 link_this_in_linux_path.sh "${pkgdir}/usr/share/java/${pkgname}/jpdfbookmarks.sh"
  install -DTm755 link_this_in_linux_path_cli.sh "${pkgdir}/usr/share/java/${pkgname}/jpdfbookmarks_cli.sh"
  install -DTm644 jpdfbookmarks.png "${pkgdir}/usr/share/icons/hicolor/128x128/apps/jpdfbookmarks.png"
  install -DTm644 ../jpdfbookmarks.desktop "${pkgdir}/usr/share/applications/jpdfbookmarks.desktop"
  install -Dm644 README "${pkgdir}/usr/share/java/${pkgname}/"

  mkdir -p "${pkgdir}/usr/bin/"
  ln -s "/usr/share/java/${pkgname}/jpdfbookmarks.sh" "${pkgdir}/usr/bin/jpdfbookmarks"
  ln -s "/usr/share/java/${pkgname}/jpdfbookmarks_cli.sh" "${pkgdir}/usr/bin/jpdfbookmarks_cli"
}

# vim:set ts=2 sw=2 et:
