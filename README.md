# SystemHelper出站阻断模块

Magisk 模块，用于禁用并阻断 `com.mobiletools.systemhelper`（中国联通 SystemHelper）的出站网络。

## 当前版本
**v1.1**

## 功能
- 开机自动禁用应用（`pm disable-user`）
- 强制停止进程
- 限制后台运行（appops）
- 按 UID 阻断所有出站流量（iptables + ip6tables）
- hosts 阻断 `dm.wo.com.cn`
- 运行日志（模块目录下 `log.txt`）
- 卸载模块时自动恢复应用并清理规则
- 支持 Magisk 内更新提示

## 下载
[SystemHelperBlocker-v1.1.zip](https://github.com/solivansprvill-droid/SystemHelper-Blocker/releases/download/v1.1/SystemHelperBlocker-v1.1.zip)

## 安装
1. 下载 zip
2. Magisk → 模块 → 从本地安装
3. 重启

## 验证
```bash
pm list packages -d | grep systemhelper
```

日志位置：`/data/adb/modules/systemhelper_blocker/log.txt`
