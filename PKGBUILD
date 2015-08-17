# Maintainer: Massimiliano Torromeo <massimiliano.torromeo@gmail.com>

pkgname=python2-requests
pkgver=0.14.1
pkgrel=1
_libname=${pkgname/python2-/}
pkgdesc="Python HTTP for Humans."
url="http://python-requests.org"
makedepends=('python2-distribute')
optdepends=('python2-certifi: SSL support'
            'python2-grequests: asynchronous requests with gevent'
            'python2-simplejson')
license=('custom: ISC')
arch=('any')
source=(http://pypi.python.org/packages/source/r/$_libname/$_libname-$pkgver.tar.gz)

build() {
    cd "$srcdir/$_libname-$pkgver"
    python2 setup.py build
}

package() {
    cd "$srcdir/$_libname-$pkgver"
    python2 setup.py install --root="$pkgdir"
	install -m0644 -D "LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

sha256sums=('4f563b907782b2c95dd2cbaf882a96133e567d46290a0e7aafa0c6f3efad19ba')
