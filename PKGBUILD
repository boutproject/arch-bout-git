# Maintainer: Ben Dudson <benjamin.dudson@york.ac.uk>
# Contributor: 

pkgname=bout++-git
pkgver=v4.1.0.r2.gdc75443e

pkgver() {
  cd "$srcdir/BOUT-dev"
  # Find most recent un-annotated tag reachable from the last commit
  git describe --long --tags | sed 's/\([^-]*-g\)/r\1/;s/-/./g'
}

pkgrel=1
pkgdesc="simulation framework in curvilinear coordinates"
arch=('x86_64')
url="https://boutproject.github.io"
license=('LGPL')

depends=('fftw' 'netcdf-cxx' 'openmpi')
makedepends=('git')
source=("git+https://github.com/boutproject/BOUT-dev.git#branch=master")
md5sums=('SKIP')

conflicts=('bout++')
provides=('bout++')

build() {
    cd "$srcdir/BOUT-dev"
    ./configure --prefix=/usr
    make
}

package() {
    cd "$srcdir/BOUT-dev"
    make DESTDIR="$pkgdir/" install
}

