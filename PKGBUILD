# Maintainer: Brieuc Roblin <brieuc dot roblin at gmail dot com>

pkgname=ucpufreq
pkgver=1.0.0.rc3
pkgrel=2
pkgdesc="Daemon providing a DBus service for accessing Cpufreq"
url="http://www.pyrotools.org/"
arch=('i686' 'x86_64')
license=('GPL')
depends=('qt' 'dbus-core' 'cpupower')
makedepends=('make')
optdepends=()
provides=('ucpufreq')
source=("http://www.pyrotools.org/software/$pkgname/$pkgname-$pkgver.tar.bz2")
md5sums=('0b50f24a8164a01802bc13e3d6d5c0ea')

build() {
  cd ${srcdir}/${pkgname}-${pkgver}
  qmake "INSTALL_PREFIX=/usr" "USE_CPUPOWER=1"
  make
}

package() {
  cd ${srcdir}/${pkgname}-${pkgver}
  make "INSTALL_ROOT=$pkgdir" install
}
