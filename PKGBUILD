# Maintainer: Megumifox <i@megumifox.com>

buildarch=28

pkgname=firmware-phicomm-n1
pkgver=6
pkgrel=1
pkgdesc="Additional firmware for Phicomm N1"
arch=('any')
url=""
license=('custom')
_commitid=96eefffcccc725425fd83be5e0704a5c32b79e54
options=('!strip')
source=('https://archlinuxarm.org/builder/src/bcm43455/7.45.154/brcmfmac43455-sdio.clm_blob'
        'https://archlinuxarm.org/builder/src/bcm43455/7.45.154/brcmfmac43455-sdio.txt'
        "https://raw.githubusercontent.com/RPi-Distro/bluez-firmware/$_commitid/broadcom/BCM4345C0.hcd")
sha256sums=('8e2250518bc789e53109728c3c0a6124bc3801a75a1cb4966125753cf1f0252e'
            '27c6b39f113f94a8c15eae63f8605e043332775c469ea072bf325773bb9ae553'
            'd09ce049f65619f007d604069d2b4d2a3ffe3cf897245287ef379955ce3969de')

package() {
  install -d "${pkgdir}/usr/lib/firmware/brcm"
  install -m 0644 *.txt *.clm_blob "${pkgdir}/usr/lib/firmware/brcm"
  install -m 0644 *.hcd "${pkgdir}/usr/lib/firmware/"
}
