# Maintainer: snql <snql DOT by AT gmail DOT com>
# Based on vivaldi-codecs-ffmpeg-extra-bin package <Maintainer: Fahad Hossain>
pkgname=yandex-browser-codecs-ffmpeg-extra-bin
pkgver=64.0.3282.119
pkgrel=1
pkgdesc="Prebuilt ffmpeg-codecs package for yandex.browser"
arch=(
  "x86_64"
)
url="https://packages.ubuntu.com/xenial/amd64/chromium-codecs-ffmpeg-extra/download"
license=('LGPL')
provides=(
  'yandex-browser-ffmpeg-codecs'
)
conflicts=(
  'yandex-browser-ffmpeg-codecs'
)
source=(
  
"http://security.ubuntu.com/ubuntu/pool/universe/c/chromium-browser/chromium-codecs-ffmpeg-extra_${pkgver}-0ubuntu0.16.04.${pkgrel}_amd64.deb"
)
md5sums=(
  "8a3117c581d4a6806aef44502173efad"
)

prepare() {
  cd "$srcdir"
  tar -xJf data.tar.xz
}

package() {
  cd "$srcdir"
  mkdir -p "$pkgdir/opt/yandex/browser-beta"
  cp "$srcdir/usr/lib/chromium-browser/libffmpeg.so" "$pkgdir/opt/yandex/browser-beta/libffmpeg.so"
}

