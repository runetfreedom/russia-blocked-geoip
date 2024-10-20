# Что это?

Этот проект каждые 6 часов автоматически генерирует GeoIP файлы, в которые включены списки заблокированных Роскомнадзором адресов и подсетей для различного рода маршрутизаторов трафика и Proxy/VPN приложений.

Источником данных на данный момент является [antifilter.download](https://antifilter.download/) и [community.antifilter.download](https://community.antifilter.download/)

На данный момент поддерживаются следующие выходные форматы:

- `geoip.dat` ([V2Ray](https://github.com/v2fly/v2ray-core), [Xray-core](https://github.com/XTLS/Xray-core), [v2rayN](https://github.com/2dust/v2rayN) и прочие)
- MaxMind `mmdb`
- [sing-box](https://github.com/SagerNet/sing-box) `srs`
- mihomo `mrs`
- Clash правила
- SURGE правила
- nginx allow и deny шаблоны

## GeoIP и MaxMind


Основные категории:

- `ru-blocked` содержит `ipresolve.lst` и `subnet.lst` сервиса antifilter.download
- `ru-blocked-community` содержит `community.lst` сервиса community.antifilter.download

Для вашего удобства в файлы включены несколько дополнительных категорий:

- `geoip:cloudflare`
- `geoip:cloudfront`
- `geoip:facebook`
- `geoip:fastly`
- `geoip:google`
- `geoip:netflix`
- `geoip:telegram`
- `geoip:twitter`
- `geoip:ddos-guard`
- `geoip:yandex`

### Содержимое файлов

- `geoip.dat`, `Country.mmdb` - содержит полный набор данных (оригинальный geoip + все категории)
- `geoip-asn.dat`, `Country-asn.mmdb` - содержит **только** дополнительные категории
- `geoip-ru-only.dat`, `Country-ru-only.mmdb` - содержит **только** списки заблокированных сетей и адресов
- `ru-blocked.dat`, `ru-blocked-community.dat` - отдельно соответствующие категории (только geoip.dat формат)
- `private.dat` - Приватные/Зарезервированные сети ([RFC6890](https://datatracker.ietf.org/doc/html/rfc6890))

### Содержимое директорий

Во всех директориях содержимое разбито по принципу "1 файл = 1 категория"

- `dat` - `geoip.dat` формат
- `text` - Текстовые списки
- `srs` - sing-box формат
- `clash` - Clash формат (включая классическую и ip-cidr нотацию)
- `mrs` - mihomo формат
- `surge` - SURGE формат
- `nginx` - allow и deny правила для nginx


# Cкачать

По данным адресам всегда доступна последняя версия файла.

- **geoip.dat**
    - [https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/geoip.dat](https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/geoip.dat)
    - [https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/geoip.dat](https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/geoip.dat)
- **geoip-asn.dat**
    - [https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/geoip-asn.dat](https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/geoip-asn.dat)
    - [https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/geoip-asn.dat](https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/geoip-asn.dat)
- **geoip-only-blocked.dat**
    - [https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/geoip-only-blocked.dat](https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/geoip-only-blocked.dat)
    - [https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/geoip-only-blocked.dat](https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/geoip-only-blocked.dat)
- **ru-blocked.dat**
    - [https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/ru-blocked.dat](https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/ru-blocked.dat)
    - [https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/ru-blocked.dat](https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/ru-blocked.dat)
- **ru-blocked-community.dat**
    - [https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/ru-blocked-community.dat](https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/ru-blocked-community.dat)
    - [https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/ru-blocked-community.dat](https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/ru-blocked-community.dat)
- **private.dat**
    - [https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/private.dat](https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/private.dat)
    - [https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/private.dat](https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/private.dat)
- **Country.mmdb**
    - [https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/Country.mmdb](https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/Country.mmdb)
    - [https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/Country.mmdb](https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/Country.mmdb)
- **Country-asn.mmdb**
    - [https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/Country-asn.mmdb](https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/Country-asn.mmdb)
    - [https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/Country-asn.mmdb](https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/Country-asn.mmdb)
- **Country-only-blocked.mmdb**
    - [https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/Country-only-blocked.mmdb](https://raw.githubusercontent.com/runetfreedom/russia-blocked-geoip/release/Country-only-blocked.mmdb)
    - [https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/Country-only-blocked.mmdb](https://cdn.jsdelivr.net/gh/runetfreedom/russia-blocked-geoip@release/Country-only-blocked.mmdb)


# Credits 

Данный репозиторий вдохновлен и частично основан на [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip)