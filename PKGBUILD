# Maintainer: Jonathan Vetter <Marchlynx@mail.de>

#pkgname=librescanner
pkgname=horus
pkgver=0.0.1
pkgrel=1
pkgdesc="Free scanner software for Ciclop Horus 3D scanner"
arch=('x86_64' 'i686' 'arm' 'armv6h' 'armv7h' 'aarch64')
url="https://github.com/bqlabs/horus"
#url="https://github.com/LibreScanner/horus"
#license=('AGPL3')
depends=('python' 'python-wxpython' 'python-pyserial' 'python-opengl' 'python-opencv'
         'python-pyglet' 'python-numpy' 'python-scipy' 'python-matplotlib'
         'v4l-utils' 'wxgtk3')
#dependencies to convert code to python3:
#python-queuelib, opencv-python, python-importlib_resources

optdepends=('avrdude: flash board firmware'
            'mjpg-streamer: stream images from webcam'
            'python-nose: debug')
provides=('horus')
conflicts=('horus')
#install=octoprint.install
source=("https://github.com/LibreScanner/horus/archive/refs/tags/0.2rc1.tar.gz")

sha256sums=('908ddd0a20e67d04854914a9cb09a0f3b9221ec1f1ee7f03d77934b4377d9952')

# horus release version:
_horusver=0.2rc1

package() {
    cd "${srcdir}/horus-${_horusver}"
    
    python setup.py install --root="$pkgdir"
}
