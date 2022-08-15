# openwrt-passwall-build

Binary distribution of [xiaorouji/openwrt-passwall](https://github.com/xiaorouji/openwrt-passwall) built for **x86/64 ONLY** with official OpenWRT **21.02** SDK.

[![Build and Release x86_64](https://github.com/paulgit/openwrt-passwall-build/actions/workflows/build-release-x86_64.yml/badge.svg)](https://github.com/paulgit/openwrt-passwall-build/actions/workflows/build-release-x86_64.yml)
[![Scan openwrt-passwall Version](https://github.com/paulgit/openwrt-passwall-build/actions/workflows/version-scan.yml/badge.svg)](https://github.com/paulgit/openwrt-passwall-build/actions/workflows/version-scan.yml)

## Install via OPKG

1. Add new opkg key:

```sh
wget https://openwrt.paulg.it/passwall.pub
opkg-key add passwall.pub
```

2. Add opkg repository:

```sh
  echo "src/gz passwall_packages https://openwrt.paulg.it/passwall/21.02/packages/x86_64/passwall_packages" >> /etc/opkg/customfeeds.conf
  echo "src/gz passwall_luci https://openwrt.paulg.it/passwall/21.02/packages/x86_64/passwall_luci" >> /etc/opkg/customfeeds.conf
  echo "src/gz passwall2 https://openwrt.paulg.it/passwall/21.02/packages/x86_64/passwall2" >> /etc/opkg/customfeeds.conf
```

3. Install package:

```sh
opkg update
opkg install luci-app-passwall
```

## Manual Install

- Download prebuilt ipk file from [openwrt.paulg.it](https://openwrt.paulg.it/).
- Upload file to your router, install it with ssh command.

```sh
opkg install luci-app-passwall*.ipk
```

## Acknowledgement

This project is heavily inspired by [kuoruan/openwrt-v2ray](https://github.com/kuoruan/openwrt-v2ray).
