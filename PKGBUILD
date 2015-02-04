pkgname='slime_vball'
pkgver=1
pkgrel=1
pkgdesc='A remake of the popular Slime Volleyball game'
arch=('i686' 'x86_64')
makedepends=('sdl' 'sdl_gfx')
license=('GPL')
url='https://bitbucket.org/parsiad/slime_vball/'

_hgroot='http://bitbucket.org/parsiad'
_hgrepo='slime_vball'

build()
{
	cd $srcdir/$_hgrepo

	autoconf configure.ac > configure || return 1
	chmod +x configure || return 1

	./configure --prefix=/usr || return 1
	make DESTDIR=$pkgdir install || return 1

	install -Dm644 slime_vball.desktop \
		$pkgdir/usr/share/applications/slime_vball.desktop
}

