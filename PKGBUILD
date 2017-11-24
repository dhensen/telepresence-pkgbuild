# Maintainer: David Stark <david@starkers.org>
# Contributor: Dino Hensen <dino.hensen@gmail.com>

pkgver=0.71
pkgrel=1
pkgname=telepresence
pkgdesc="Local development against a remote Kubernetes or OpenShift cluster - http://www.telepresence.io"
arch=('any')
license=('Apache')
url="https://github.com/datawire/telepresence"
makedepends=()
backup=()
depends=(
    'conntrack-tools'
    'git'
    'python'
    'python-virtualenv'
    'socat'
    'sshfs'
    'torsocks'
    )

source=("https://github.com/datawire/telepresence/archive/${pkgver}.tar.gz")
md5sums=('SKIP')

build(){
  cd "${srcdir}/${pkgname}-${pkgver}"
  make setup
}

package(){
  install -Dm 755 "${srcdir}/${pkgname}-${pkgver}/cli/telepresence" "${pkgdir}/usr/bin/telepresence"
  install -Dm 755 "${srcdir}/${pkgname}-${pkgver}/cli/stamp-telepresence" "${pkgdir}/usr/bin/stamp-telepresence"
  install -Dm 755 "${srcdir}/${pkgname}-${pkgver}/virtualenv/bin/sshuttle-telepresence" "${pkgdir}/usr/bin/sshuttle-telepresence"
}

# vim:set ts=2 sw=2 et: