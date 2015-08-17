# Maintainer: lilydjwg <lilydjwg@gmail.com>
# Contributor: Felipe Morales <hel.sheep@gmail.com>
# Based on the packaging of Frank Smit <frank@61924.nl> (redis-py-git on AUR)

_gitname=python-magic
pkgname=python-magic-git
pkgver=0.4.3.29_g0d8f718
pkgrel=1
pkgdesc="A python wrapper for libmagic. git version"
arch=('any')
url="https://github.com/ahupp/python-magic"
license=('PSF')
depends=('python' 'python-setuptools')
makedepends=('git')
source=("git://github.com/ahupp/$_gitname.git")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$_gitname"
  git describe --tags | sed 's/-/./;s/-/_/g'
}

package() {
  cd "$srcdir/$_gitname"
  python3 setup.py install --root="$pkgdir/" --optimize=1
}

