# OpenWrt PassWall All Mirror

This repository automatically syncs the following upstream repositories:

- Openwrt-Passwall/openwrt-passwall
- Openwrt-Passwall/openwrt-passwall-packages
- Openwrt-Passwall/openwrt-passwall2

## Directory structure

```text
openwrt-passwall-all
├── openwrt-passwall
├── openwrt-passwall-packages
└── openwrt-passwall2
```

## Usage in OpenWrt buildroot

Add the following line to feeds.conf.default:

```bash
src-git passwall_all https://github.com/liuxindavid/openwrt-passwall-all.git;main
```

Then run:

```bash
./scripts/feeds update passwall_all
./scripts/feeds install -a -p passwall_all
```

## Notes

The upstream .github directories are removed to avoid GitHub workflow permission issues.
Tags are not synchronized. Only the latest main branch contents are mirrored.
