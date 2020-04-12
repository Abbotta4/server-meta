# Maintainer: Abbott <abbotta4@gmail.com>
pkgname=system-config
pkgver=1.0.0
pkgrel=1
pkgdesc="non-user configs"
arch=("any")
license=("custom")
depends=("nginx" "openvpn" "php" "php72")

source=('drew.abbotts.site'
        'etc-nginx-sites-available-drew.abbotts.site'
        'etc-nginx-sites-available-justthelads.party'
        'etc-nginx-sites-available-nginx.conf'
        'etc-nginx-sites-available-redirects'
        'etc-nginx-sites-available-rtorrent'
        'etc-nginx-sites-available-rutorrent'
        'etc-openvpn-server-forward.conf'
        'etc-openvpn-server-noforward.conf'
)

package() {
        # nginx
        install -Dm0644 etc-nginx-sites-available-drew.abbotts.site "$pkgdir"/etc/nginx/sites-available/drew.abbotts.site
        install -Dm0644 etc-nginx-sites-available-justthelads.party "$pkgdir"/etc/nginx/sites-available/justthelads.party
        install -Dm0644 etc-nginx-nginx.conf "$pkgdir"/etc/nginx/nginx.conf
        install -Dm0644 etc-nginx-sites-available-redirects "$pkgdir"/etc/nginx/sites-available/redirects
        install -Dm0644 etc-nginx-sites-available-rtorrent "$pkgdir"/etc/nginx/sites-available/rtorrent
        install -Dm0644 etc-nginx-sites-available-rutorrent "$pkgdir"/etc/nginx/sites-available/rutorrent
	ln -sf "$pkgdir"/etc/nginx/sites-available/drew.abbotts.site "$pkgdir"/etc/nginx/sites-enabled/drew.abbotts.site
	ln -sf "$pkgdir"/etc/nginx/sites-available/justthelads.party "$pkgdir"/etc/nginx/sites-enabled/justthelads.party
	ln -sf "$pkgdir"/etc/nginx/sites-available/redirects "$pkgdir"/etc/nginx/sites-enabled/redirects
	ln -sf "$pkgdir"/etc/nginx/sites-available/rtorrent "$pkgdir"/etc/nginx/sites-enabled/rtorrent
	# openvpn	
install -Dm0644 etc-openvpn-server-forward.conf "$pkgdir"/etc/openvpn/server/forward.conf
	install -Dm0644 etc-openvpn-server-noforward.conf "$pkgdir"/etc/openvpn/server/noforward.conf
    }

sha1sums=('d383a84c6f542246c8a12b355146c26bd1a51698'
          '4e369daf0c01208cf897c7229ceda811f54c6949'
          'a4ebf6311b22a0cac80b8fca0de20b092967bacf'
          'b85356eed555497931802a08d766a2fa22371af0'
          '14819da01bd9ff6922cd881f61fa1a5a184dd470'
          '2a369e898c63830faf36bf185c8b6cba8c6272c0'
	  '0aa37b76113b4062ca2b84712f3ecf6df5a3e87e'
          '96bc5a671313a3cdc9917f72d7114f4048be5f18')