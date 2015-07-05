# Maintainer: BlackEagle < ike DOT devolder AT gmail DOT com >
pkgname=php-mongo
pkgver=1.4.1
pkgrel=1
pkgdesc="Officially supported PHP driver for MongoDB"
arch=("i686" "x86_64")
url="http://www.mongodb.org/display/DOCS/PHP+Language+Center"
license=("APACHE")
depends=("php")
backup=("etc/php/conf.d/mongo.ini")
source=(
	"http://pecl.php.net/get/mongo-$pkgver.tgz"
	"mongo.ini"
)

package() {
	cd mongo-$pkgver
	phpize
	./configure --prefix=/usr --enable-mongo
	make INSTALL_ROOT="$pkgdir" install
	install -Dm644 "$srcdir/mongo.ini" "$pkgdir/etc/php/conf.d/mongo.ini"
}
sha256sums=('230e7d26eaa826c7aacfc90fd1128f8c390216abe7f588d3bbcd130bd1fb84b6'
            'c89685eee842d5c3a85149a5bb8e310e62bf1a17f94183bb66401593ab2b191b')
