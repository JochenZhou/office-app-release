# 宏智汇云助手 · 升级发布仓库

本仓库是 [office-app](https://github.com/JochenZhou/office-app)（宏智汇云助手 Android App）的
**公开发布通道**（备份通道），由源仓库 CI 自动更新：

- `latest.json` — 正式版清单（App 自动「检查更新」读它）
- `prerelease.json` — 预发布清单（App 手动「查询预发布版本」读它，普通用户看不到）
- `office-app-vX.Y.Z.apk` — 正式版安装包（只保留最新一个）
- `office-app-vX.Y.Z-rcN.apk` — 预发布安装包（只保留最新一个）
- `materials/` — 资料库热更新镜像（App 内的资料按需下载）

## 为什么没有历史提交

每次发版都会提交一个 20+ MB 的安装包，正常提交历史会让仓库迅速膨胀到几百 MB。
所以本仓库在**每次发布时都把历史压平**（`git checkout --orphan` + force push，历史只保留最新快照）——
仓库体积永远等于「最新快照」的大小。

需要旧版本安装包请到源仓库的 Releases 页面（`JochenZhou/office-app`）。

## latest.json 结构

```json
{
  "version": "v1.38.1",
  "date": "2026-09-23",
  "apkUrl": "https://ghfast.top/https://raw.githubusercontent.com/JochenZhou/office-app-release/main/office-app-v1.38.1.apk",
  "apkUrlBackup": "https://raw.githubusercontent.com/JochenZhou/office-app-release/main/office-app-v1.38.1.apk",
  "apkSize": 24697663,
  "apkSha256": "24e42654…",
  "notes": "更新说明"
}
```

> 本仓库只存放发布产物，不含源码与任何凭证。
> 注：v1.8.1 及更早的 APK 为 CI 随机 debug 签名，升级到 v1.8.2+ 前需先卸载旧版（仅此一次）。
