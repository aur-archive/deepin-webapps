# Maintainer: Xu Fasheng <fasheng.xu[AT]gmail.com>

### MERGE TO ONE PACKAGE FOR AUR
pkgname='deepin-webapps'
pkgdesc="Web apps from Linux Deepin"
depends=('chromium' 'xdg-utils')

# pkgname=('deepin-webapps-kuwo-music'
#          'deepin-webapps-dbank-online-storage'
#          'deepin-webapps-youdao-note'
#          'deepin-webapps-chainrxn'
#          'deepin-webapps-doit-im'
#          'deepin-webapps-microsoft-skydrive'
#          'deepin-webapps-baidu-map'
#          'deepin-webapps-douban'
#          'deepin-webapps-ttpod'
#          'deepin-webapps-kugou-music'
#          'deepin-webapps-kingsoft-fast-docs'
#          'deepin-webapps-xiami-music'
#          'deepin-webapps-cargo-bridge'
#          'deepin-webapps-sina-weibo'
#          'deepin-webapps-pirateslovedaisies'
#          'deepin-webapps-kingsoft-online-storage'
#          'deepin-webapps-baidu-music'
#          'deepin-webapps-baidu-online-storage'
#          'deepin-webapps-paulrouget'
#          'deepin-webapps-towerim'
#          'deepin-webapps-fetion'
#          'deepin-webapps-baidu-hi'
#          'deepin-webapps-12306')
# pkgbase="deepin-webapps"
pkgver=0.7
pkgrel=1
arch=('i686' 'x86_64')
url="http://www.linuxdeepin.com/"
license=('GPL2')
# depends=('chromium' 'xdg-utils')

source=("$http://packages.linuxdeepin.com/deepin/pool/main/d/deepin-webapps/deepin-webapps_0.7.orig.tar.xz")
md5sums=('e4019e5f8dc50342fb85e9877d939ea4')

_install_copyright_and_changelog() {
    mkdir -p "${pkgdir}/usr/share/doc/${pkgname}"
    cp -f debian/copyright "${pkgdir}/usr/share/doc/${pkgname}/"
    gzip -c debian/changelog > "${pkgdir}/usr/share/doc/${pkgname}/changelog.gz"
}

# Usage: _easycp dest files...
_easycp () {
    local dest=$1; shift
    mkdir -p "${dest}"
    cp -R -t "${dest}" "$@"
}

_package_webapp() {
    cd "${srcdir}"
    local _appname="${pkgname#deepin-webapps-}"
    local _icon=${1:-"${_appname}.png"}
    local _html=${2:-"${_appname}.html"}
    local _desktop=${3:-"${_appname}.desktop"}

    _easycp "${pkgdir}"/usr/share/icons/hicolor/48x48/apps/ icons/"${_icon}"
    _easycp "${pkgdir}"/usr/share/deepin-webapps/ html/"${_html}"

    mkdir -p "${pkgdir}"/usr/share/applications
    install -m 0644 desktops/"${_desktop}" "${pkgdir}"/usr/share/applications/

    _install_copyright_and_changelog

    # run with chromium
    sed -i 's_Exec=/usr/bin/google-chrome_Exec=/usr/bin/chromium_' \
        "${pkgdir}"/usr/share/applications/"${_desktop}"
}

package_deepin-webapps-kuwo-music() {
    pkgdesc="Kuwo Music - Kuwo Web Music"
    _package_webapp "kuwo.png"
}

package_deepin-webapps-dbank-online-storage() {
    pkgdesc="DBank Online Storage - Store your files using DBank Online Storage"
    _package_webapp
}

package_deepin-webapps-youdao-note() {
    pkgdesc="Youdao Note - Remember with Youdao Note"
    _package_webapp
}

package_deepin-webapps-chainrxn() {
    pkgdesc="Chain Reaction - an addictive game that is very simple: Clear the level of bombs."
    _package_webapp "chain-reaction.png"
}

package_deepin-webapps-doit-im() {
    pkgdesc="Doit.im - Best Online GTD Service for Getting Things Done, Always Online, Always With You!"
    _package_webapp
}

package_deepin-webapps-microsoft-skydrive() {
    pkgdesc="Microsoft SkyDrive - Edit,save files and coperate online"
    _package_webapp "microsoft.png"
}

package_deepin-webapps-baidu-map() {
    pkgdesc="Baidu Map - Baidu Map Service for China"
    _package_webapp
}

package_deepin-webapps-douban() {
    pkgdesc="Douban FM - Douban Music Service"
    _package_webapp
}

package_deepin-webapps-ttpod() {
    pkgdesc="ttpod - ttpod web"
    _package_webapp
}

package_deepin-webapps-kugou-music() {
    pkgdesc="Kugou Music - Kugou Online Music"
    _package_webapp
}

package_deepin-webapps-kingsoft-fast-docs() {
    pkgdesc="Kingsoft Fast Docs - Edit and save documents online"
    _package_webapp
}

package_deepin-webapps-xiami-music() {
    pkgdesc="Xiami Music - Xiami Music in China"
    _package_webapp "xiami.png"
}

package_deepin-webapps-cargo-bridge() {
    pkgdesc="Cargo Bridge - A new quality of bridge builder. Build a bridge and test your construction skills."
    _package_webapp
}

package_deepin-webapps-sina-weibo() {
    pkgdesc="Sina Weibo - China Popular SNS which is like twitter"
    _package_webapp "weibo.png"
}

package_deepin-webapps-pirateslovedaisies() {
    pkgdesc="Description: Pirates Love Daisies - Davey Jones is sending his minions to collect your most precious resource, your Daisies!! Hire a crew, and use them to thwart the creeps."
    _package_webapp "pirates-love-daisies.png"
}

package_deepin-webapps-kingsoft-online-storage() {
    pkgdesc="Kingsoft Online Storage - Store your files using Kingsoft Online Storage"
    _package_webapp
}

package_deepin-webapps-baidu-music() {
    pkgdesc="Baidu Music - Baidu Web Music"
    _package_webapp
}

package_deepin-webapps-baidu-online-storage() {
    pkgdesc="Baidu Online Storage - Store your files using Baidu Storage"
    _package_webapp
}

package_deepin-webapps-paulrouget() {
    pkgdesc="Runfield - A simple yet wacky HTML5 game demo in which you take the role of a hyper fox."
    _package_webapp
}

package_deepin-webapps-towerim() {
    pkgdesc="Tower.im - 简单好用的团队协作工具"
    _package_webapp
}

package_deepin-webapps-fetion() {
    pkgdesc="Fetion - Chat with friends using Fetion"
    _package_webapp
}

package_deepin-webapps-baidu-hi() {
    pkgdesc="Baidu Hi - Baidu IM Client"
    _package_webapp
}

package_deepin-webapps-12306() {
    pkgdesc="12306"
    _package_webapp
}

### MERGE TO ONE PACKAGE FOR AUR
package() {
    local webapps="kuwo-music dbank-online-storage youdao-note chainrxn doit-im microsoft-skydrive baidu-map douban ttpod kugou-music kingsoft-fast-docs xiami-music cargo-bridge sina-weibo pirateslovedaisies kingsoft-online-storage baidu-music baidu-online-storage paulrouget towerim fetion baidu-hi 12306"

    for app in $webapps; do
        local pkgname="${app}"
        eval package_deepin-webapps-"${pkgname}"
    done

    # overwrite variables again, or upload to aur may be failed
    pkgname='deepin-webapps'
    pkgdesc="Web apps from Linux Deepin"
    depends=('chromium' 'xdg-utils')
}
