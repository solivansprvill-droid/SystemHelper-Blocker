# SystemHelperBlocker

Magisk module to disable and block outbound network of `com.mobiletools.systemhelper` (China Unicom SystemHelper).

## Features
- Automatically disables the app on boot (`pm disable-user`)
- Blocks all outbound traffic by UID via iptables + ip6tables
- Hosts block for `dm.wo.com.cn`
- Cleans up rules and re-enables the app on module uninstall

## Download
[SystemHelperBlocker-v1.0.zip](https://github.com/solivansprvill-droid/SystemHelperBlocker/releases/download/v1.0/SystemHelperBlocker-v1.0.zip)

## Install
1. Download the zip
2. Magisk → Modules → Install from storage
3. Reboot

## Verify
```bash
pm list packages -d | grep systemhelper
```
