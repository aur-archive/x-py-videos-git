# Author: Darth O-Ring
# Maintainer: Chubby_Lover <chubbyloverb@gmail.com>
pkgname='x-py-videos-git'
_gitname="xpyvideos"
pkgver=v0.0.3.3.r0.gfb61d31
pkgrel=1
pkgdesc="Python program for downloading videos from xvideos, xhamster, redtube, and youtube."
arch=('any')
url="https://github.com/Darth-O-Ring/xpyvideos"
license=('GPL')
depends=('python2')
makedepends=('git')
provides=('xpyvideos' 'pytube')
conflicts=('xpyvideos' 'pytube')
source=("git://github.com/Darth-O-Ring/xpyvideos.git")
md5sums=('SKIP') #generate with 'makepkg -g'

pkgver() {
  cd "${srcdir}/${_gitname}"
  git describe --long --tags | sed -r 's/([^-]*-g)/r\1/;s/-/./g'
}


package() {
	cd "${srcdir}/${_gitname}"
	python2 setup.py install --root="${pkgdir}" --optimize=1
}




# vim:set ts=2 sw=2 et:

