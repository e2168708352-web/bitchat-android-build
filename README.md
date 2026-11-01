# bitchat Android builds

bitchat 安卓端的发布仓库：从上游官方发布同步已签名的 universal APK，并提供
GitHub Actions 云构建工作流。上游项目：
[permissionlesstech/bitchat-android](https://github.com/permissionlesstech/bitchat-android)。

> 双端统一下载页：**https://e2168708352-web.github.io/bitchat-android-build/**

## 下载

| 平台 | 版本 | 文件 | 说明 |
| --- | --- | --- | --- |
| Android | 2.2.0 | [bitchat-2.2.0.apk](https://github.com/e2168708352-web/bitchat-android-build/releases/download/v2.2.0/bitchat-2.2.0.apk) | 官方签名 universal APK，可直接安装 |
| iOS | 1.8.0 | [bitchat-unsigned.ipa](https://github.com/e2168708352-web/bitchat-ios-build/releases/download/v1.8.0/bitchat-unsigned.ipa) | 未签名，需自签，见 [iOS 仓库](https://github.com/e2168708352-web/bitchat-ios-build) |

完整说明与校验值见 [统一下载页](https://e2168708352-web.github.io/bitchat-android-build/)，
或本仓库的 [Releases](https://github.com/e2168708352-web/bitchat-android-build/releases) 页面。

## 安装注意

- 官方签名的 2.2.0 可直接安装。
- 如果手机上装的是本仓库此前构建的 **debug 签名 2.1.0**，签名不同无法覆盖安装，
  需先卸载旧版；卸载前建议先备份聊天身份数据。
- debug 版仅用于自测，不建议日常使用。

## 云构建

- 工作流：[`.github/workflows/build-apk.yml`](.github/workflows/build-apk.yml)
- 手动触发：**Actions → Build bitchat APK → Run workflow**，`source_ref` 支持分支、标签或提交 SHA。
- 产物为 debug 签名的 APK，保留 1 天，仅作验证用途，不作为发布包。

## 来源声明

Releases 中的 Android APK 同步自上游官方发布，未做任何修改，签名证书 SHA-256 为
`3b03fa66a5451321100792f5b55a7b4966d5c8dc10c6daa40aa95ea489531bca`。
本仓库与 bitchat 维护者无隶属关系。
