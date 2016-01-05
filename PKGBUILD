# Maintainer: Olivier Biesmans <olivier at biesmans dot fr>
pkgname=butterfly
pkgver=2.0.0
pkgrel=1
pkgdesc="A sleek web based terminal emulator"
arch=('any')
url="https://pypi.python.org/pypi/butterfly"
license=('GPL')
groups=()
depends=('python' 'python-tornado' 'python-pyopenssl' 'tornado_systemd' 'python-libsass')
makedepends=('python-setuptools')
provides=()
conflicts=()
replaces=()
backup=()
options=(!emptydirs)
install=
source=("https://pypi.python.org/packages/source/b/butterfly/butterfly-${pkgver}.tar.gz" "butterfly.service")
sha256sums=('d2040520d7ba0f83b2dee60a45ce83066ba3a83f74fd79cc11d46b79c4e093ff'
            '2e4fe822908270db8648bcdb492025ab4b972007860a92393b4d4313d6598dbe')

package() {
  cd "$srcdir/$pkgname-$pkgver"
  python setup.py install --root="$pkgdir/" --optimize=1
  install -Dm 0644 "${srcdir}/${pkgname}.service" \
    "$pkgdir/etc/systemd/system/${pkgname}.service"
}

# vim:set ts=2 sw=2 et:
