# 🧱 APK 打包器

上传 Android Studio 项目 ZIP 到这个仓库，GitHub 云端会自动编译成 APK。

## 怎么用（三步）
1. 点仓库页面的 **Add file → Upload files**
2. 把你的 Android 项目打包成 `.zip`，拖进来，点 **Commit changes**
3. 等几分钟，点上方 **Actions** 标签 → 看任务变绿 → 点进去 → 底部 **Artifacts → APK成品** 下载

## 自动检查什么
- ZIP 是否合法
- 是否包含 Android 项目关键文件（settings.gradle / build.gradle / app/build.gradle / AndroidManifest.xml）
- 缺文件会直接编译失败并在日志里提示

## 环境
- JDK 17 + Gradle 8.7
- 支持 compileSdk 34 / 35
- 项目带 gradlew 会优先使用 gradlew

## 注意
- 每次上传新的 zip 都会自动触发重新编译
- 编译失败请点进 Actions 任务查看日志，常见原因是 Gradle/SDK 版本不匹配
- 
