# 手环电子书同步器（安卓端）

配套 [com.bandbbs.ebook](https://github.com/lewb521/com.bandbbs.ebook)（手环端电子书阅读器）的安卓同步客户端，用于把手机上的 txt 电子书推送到小米手环阅读。

## 功能

- 选择手机里的 txt 电子书
- 通过小米互联 SDK 与手环端握手，远程打开 `pages/push` 路由并传输
- 支持中文字符编码自动识别（juniversalchardet）

## 使用步骤

1. 手环已安装并打开手环端应用；手机与手环已在小米运动健康中配对。
2. 打开同步器，选择要推送的 txt 电子书。
3. 确认后自动连接手环并开始传输，手环端进入同步页接收。

## 构建

环境要求：JDK 17、Android SDK（`compileSdk = 36`）。

1. 在项目根目录放入你的签名文件：
   - `watchface.keystore`
   - `keystore.properties`（内容包含 `storePassword`、`keyAlias`、`keyPassword`）
2. 执行：

```bash
./gradlew assembleDebug
# 产物：app/build/outputs/apk/debug/app-debug.apk
```

## 安装包

仓库根目录 `release/` 提供已签名 APK（`com.bandbbs.ebook-android-3.0.25.5.27.apk`），可直接安装。

## 开源许可

AGPL-3.0，详见 [LICENSE](./LICENSE)。

## 上游出处

本项目基于 [BandBBS-Vela-Dev/com.bandbbs.ebook-android](https://github.com/BandBBS-Vela-Dev/com.bandbbs.ebook-android)（喵喵电子书同步器）。