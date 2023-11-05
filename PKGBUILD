# Maintainer: Torsten Evers <tevers@onlinehome.de>

pkgname=mesa-nw-vf2
pkgdesc="an open-source implementation of the OpenGL specification, PowerVR (VisionFive2) version, nightwulf experimental version"
pkgver=22.3.5
pkgrel=2
arch=('riscv64')
makedepends=('git' 'python-mako' 'xorgproto'
              'libxml2' 'libx11'  'libvdpau' 'libva' 'elfutils' 'libxrandr'
              'wayland-protocols' 'meson' 'ninja' 'glslang' 'directx-headers' )
depends=('libdrm' 'libxxf86vm' 'libxdamage' 'libxshmfence' 'libelf'
         'libomxil-bellagio' 'libunwind' 'libglvnd' 'wayland' 'lm_sensors' 'vulkan-icd-loader' 'zstd' 'expat'
	 'llvm15')
optdepends=('opengl-man-pages: for the OpenGL API man pages')
provides=('mesa' 'vulkan-mesa-layer' 'vulkan-driver' 'mesa-libgl' 'opengl-driver')
conflicts=('mesa' 'vulkan-mesa-layer' 'mesa-libgl')
url="https://www.mesa3d.org"
license=('custom')
source=("mesa_debian.tar.gz")
install="llvm-link.install"
sha256sums=('8f2321dc9786c133826977397fd9c941296fd2044c04f50f3c1fc7fe65e30a3b')

package () {
    mkdir -p "${pkgdir}/usr"
    cp -a "${srcdir}/usr/bin" "${pkgdir}/usr"
    cp -a "${srcdir}/usr/include" "${pkgdir}/usr"
    cp -a "${srcdir}/usr/share" "${pkgdir}/usr"
    mkdir -p "${pkgdir}/usr/lib"
    cp -a "${srcdir}/usr/lib/riscv64-linux-gnu/"* "${pkgdir}/usr/lib/"
}

