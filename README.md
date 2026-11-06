# SystemHelper出站阻断模块

Magisk 模块，用于禁用并阻断以下组件的出站网络：

- `com.mobiletools.systemhelper`（中国联通 SystemHelper）
- `com.miui.guardprovider`（小米系统安全组件）

## 当前版本
**v1.2**

## 功能
- 开机自动禁用应用（`pm disable-user`）
- 强制停止进程
- 限制后台运行（appops）
- 按 UID 阻断所有出站流量（iptables + ip6tables）
- hosts 阻断相关域名
- 运行日志（模块目录下 `log.txt`）
- 卸载模块时自动恢复

## 下载
[SystemHelperBlocker-v1.2.zip](https://github.com/solivansprvill-droid/SystemHelper-Blocker/releases/download/v1.2/SystemHelperBlocker-v1.2.zip)

## 安装
1. 下载 zip
2. Magisk → 模块 → 从本地安装
3. 重启

## 注意
禁用系统安全组件可能影响侧载 / ADB 安装确认提示。如有异常，卸载本模块即可恢复。

## 验证
```bash
pm list packages -d | grep -E "systemhelper|guardprovider"
```

日志位置：`/data/adb/modules/systemhelper_blocker/log.txt`
