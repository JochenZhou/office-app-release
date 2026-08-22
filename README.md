# 宏智汇云助手 · 升级发布仓库

本仓库是 [office-app](https://github.com/JochenZhou/office-app)（宏智汇云助手 Android App）的
**公开发布通道**，由源仓库 CI 在打 `v*` 标签发版时自动更新：

- `app-debug.apk` — 最新版本安装包
- `latest.json` — 版本信息（供 App 内「检查更新」匿名读取）

## latest.json 结构

```json
{
  "version": "v1.7.0",
  "date": "2026-08-22",
  "apkUrl": "https://raw.githubusercontent.com/JochenZhou/office-app-release/main/app-debug.apk",
  "notes": "更新说明"
}
```

> 本仓库只存放发布产物，不含源码与任何凭证。
