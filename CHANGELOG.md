<!-- Keep a Changelog guide -> https://keepachangelog.com -->

# FishPi Chat Changelog

## [Unreleased]

## [1.0.0] - 2025-01-XX

### 🎉 重大更新
- **品牌重命名**: PWL Chat → FishPi Chat
- **兼容性大幅提升**: 支持 IntelliJ IDEA 2023.1 - 2025.1

### 🔧 技术升级
- 升级 Kotlin 版本至 1.9.25
- 升级 Java 版本要求至 17
- 升级 Gradle IntelliJ Plugin 至 1.17.4
- 升级所有核心依赖库：
  - OkHttp: 3.14.4 → 4.12.0
  - Gson: 2.8.5 → 2.11.0
  - Jsoup: 1.14.2 → 1.18.3
  - Java-WebSocket: 1.5.2 → 1.5.7
  - SLF4J: 1.7.25 → 2.0.16

### 🐛 修复
- 修复新版本 IDEA 的兼容性问题
- 解决插件加载失败的问题
- 优化性能和稳定性

### ⚠️ 破坏性变更
- 插件 ID 变更: `com.github.danbai225.pwlchat` → `com.github.danbai225.fishpichat`
- 工具窗口名称: `PWL` → `FishPi`

## [0.3.1] - 2023-XX-XX

- wss url获取

## [0.3.0] - 2023-XX-XX

- 客户端标识

## [0.2.0] - 2023-XX-XX

- web view记录数限制（200）
- 活跃度进度条更新
- web view点歌卡死

## [0.1.8] - 2022-XX-XX

- auto_packet 自动打开红包 控制开关命令