# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Jochen Schalanda <jochen+aur@schalanda.name>
# Contributor: Anatol Pomozov <anatol.pomozov@gmail.com>
# Contributor: Alexsandr Pavlov <kidoz at mail dot ru>

_gemname=multi_json
pkgname=ruby-$_gemname-1.8
pkgver=1.8.4
pkgrel=1
pkgdesc='A common interface to multiple JSON libraries.'
arch=(any)
url='https://github.com/intridea/multi_json'
license=(MIT)
depends=(ruby)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha256sums=('011a3868b5179a3c8bc87b6f3568124d6e2ee0d4f19321ce8c976b0668164585')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE.md" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.md"
}
