
pkgname=toluapp
pkgver=1.0.93
_commit=b34075b76835b778bb6b2ce0aa224afd9d182887
pkgrel=1
pkgdesc="Extension of toLua, a tool to integrate C/C++ code with Lua."
arch=('x86_64')
url="https://github.com/LuaDist/toluapp"
license=('MIT')
depends=('lua')
makedepends=('cmake')
conflicts=('tolua++')
replaces=('tolua++')
provides=('tolua++')
source=("https://github.com/LuaDist/toluapp/archive/${_commit}.zip")
md5sums=('7f94eb48fa01693111e3d15b4fde8bbf')

build() {
    mkdir -p build
    cd build

    cmake ../${pkgname}-${_commit} \
        -DCMAKE_INSTALL_PREFIX=/usr 
}

package() {
    cd build

    make DESTDIR=${pkgdir} install

    install -Dm644 ${srcdir}/toluapp-${_commit}/COPYRIGHT ${pkgdir}/usr/share/licenses/${pkgname}/COPYRIGHT
}
