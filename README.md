# 宏智汇云助手 · 升级发布仓库

本仓库是 [office-app](https://github.com/JochenZhou/office-app)（宏智汇云助手 Android App）的
**公开发布通道**，由源仓库 CI 在打 `v*` 标签发版时自动更新：

- `app-release.apk` — 最新版本安装包（v1.8.2 起使用固定签名，可覆盖安装）
- `latest.json` — 版本信息（供 App 内「检查更新」匿名读取）

## latest.json 结构

```json
{
  "version": "v1.8.2",
  "date": "2026-08-22",
  "apkUrl": "https://raw.githubusercontent.com/JochenZhou/office-app-release/main/app-release.apk",
  "notes": "更新说明"
}
```

> 本仓库只存放发布产物，不含源码与任何凭证。
> 注：v1.8.1 及更早的 APK 为 CI 随机 debug 签名，升级到 v1.8.2+ 前需先卸载旧版（仅此一次）。
