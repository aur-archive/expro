# Maintainer: ninian <mcfadzean.org.uk ta linux>

pkgname=expro
pkgver=2.7.0
pkgrel=4
pkgdesc="Opens objects in associated applications by matching regular expressions against object name or MIME-type"
arch=('any')
url="http://appstogo.mcfadzean.org.uk/linux.html#expro"
license=('MIT')
depends=('bash' 'dmenu' 'libnotify' 'file')
optdepends=('gxmessage: for displaying rather than executing' 'sudo: for executing as root')
backup=('etc/expro.conf')
source=("http://appstogo.mcfadzean.org.uk/dl/$pkgname/$pkgname-$pkgver.tar.gz")
md5sums=('8ae0004398059cc661d80e55d5300dad')

package() {
  cd "$srcdir/$pkgname-$pkgver"

  # script
  install -Dm755 $pkgname "$pkgdir/usr/bin/$pkgname"
  # uncomment the following 3 lines if you wish expro to provide xdg-open and/or xdg-email
  # mkdir -p "$pkgdir/usr/local/bin"
  # ln -s "/usr/bin/$pkgname" "$pkgdir/usr/local/bin/xdg-open" 
  # ln -s "/usr/bin/$pkgname" "$pkgdir/usr/local/bin/xdg-email" 

  # configuration
  install -Dm644 $pkgname.conf "$pkgdir/etc/$pkgname.conf"
  msg "Remember to customize $pkgname.conf after installation"

  # licensing
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
