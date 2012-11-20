# http://github.com/antoinemartin/ec2-systemd-init
pkgname=ec2-systemd-init
pkgver=1.0
pkgrel=1
pkgdesc="systemd initialization scripts for EC2"
arch=(any)
url="http://github.com/antoinemartin/ec2-systemd-init"
license=('BSD')
depends=(systemd)
source=('ec2'
        'ec2.service')

build() {
    cd "$srcdir"
}

package() {
    cd "$srcdir"

    install -m 0755 -d "$pkgdir/usr/lib/systemd/system"
    install -m 0644 ec2.service "$pkgdir/usr/lib/systemd/system"

    install -m 0755 -d "$pkgdir/etc"
    install -m 0700 ec2 "$pkgdir/etc"
}

#=
md5sums=('72826b95cc26db82f711327174dd6f2b'
         '71ac5a9175e352f2d08704a660d0e83a')
