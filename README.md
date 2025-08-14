# FishPi Chat - 摸鱼派聊天插件

[![Build](https://github.com/danbai225/pwl-chat/workflows/Build/badge.svg)](https://github.com/danbai225/pwl-chat/actions)
[![Version](https://img.shields.io/jetbrains/plugin/v/com.github.danbai225.fishpichat.svg)](https://plugins.jetbrains.com/plugin/18091-pwl-chat)
[![Downloads](https://img.shields.io/jetbrains/plugin/d/com.github.danbai225.fishpichat.svg)](https://plugins.jetbrains.com/plugin/18091-pwl-chat)
[![License](https://img.shields.io/github/license/danbai225/pwl-chat)](https://github.com/danbai225/pwl-chat/blob/main/LICENSE)

## 📖 项目简介

FishPi Chat 是一个专为 IntelliJ IDEA 系列 IDE 设计的聊天插件，让开发者可以在不离开开发环境的情况下，直接与[摸鱼派](https://fishpi.cn)社区的朋友们进行实时交流。无论是技术讨论、日常闲聊还是红包互动，都可以在熟悉的 IDE 界面中轻松完成。

<!-- Plugin description -->
This is a [FishPi](https://fishpi.cn) chat plugin.

这是一个连接[摸鱼派](https://fishpi.cn/)的聊天插件，让你在 IDE 中与社区朋友实时交流。
<!-- Plugin description end -->

## ✨ 主要特性

### 💬 聊天功能
- **实时消息收发** - 基于 WebSocket 的实时通信
- **双显示模式** - 支持文本模式和富文本Web模式
- **消息历史** - 自动加载聊天历史记录
- **在线用户** - 实时显示在线用户列表，双击@用户
- **消息撤回** - 支持撤回最后发送的消息

### 🧧 红包系统
- **发送红包** - 支持自定义金额、数量和祝福语
- **自动抢红包** - 可配置的自动抢红包功能
- **红包提醒** - 红包消息特殊显示和提醒

### 🎯 智能功能
- **活跃度显示** - 实时显示当前活跃度进度
- **命令系统** - 丰富的命令行操作支持
- **用户名联想** - 输入@时自动联想用户名
- **文件上传** - 支持图片和文件上传分享
- **消息历史** - 方向键快速切换历史输入

### 🔧 个性化配置
- **显示模式切换** - 文本模式 ↔ Web模式
- **消息提醒控制** - 可配置各类消息提醒
- **自动抢红包开关** - 灵活控制自动抢红包
- **事件日志输出** - 可选择在IDE事件中显示聊天消息

## 🚀 安装方式

### 方式一：IDE插件市场（推荐）
1. 打开 IntelliJ IDEA
2. 进入 <kbd>File</kbd> → <kbd>Settings</kbd> → <kbd>Plugins</kbd>
3. 点击 <kbd>Marketplace</kbd> 标签
4. 搜索 `fishpi-chat`
5. 点击 <kbd>Install</kbd> 安装

### 方式二：手动安装
1. 从 [Releases](https://github.com/danbai225/pwl-chat/releases/latest) 下载最新版本
2. 进入 <kbd>File</kbd> → <kbd>Settings</kbd> → <kbd>Plugins</kbd>
3. 点击 <kbd>⚙️</kbd> → <kbd>Install Plugin from Disk...</kbd>
4. 选择下载的插件文件并安装

## 🎮 使用指南

### 首次使用
1. 安装插件后重启IDE
2. 在底部工具栏找到 `FishPi` 面板
3. 点击 `Login` 按钮
4. 输入摸鱼派账号和密码
5. 如有二步验证，输入验证码（无则忽略）
6. 登录成功后即可开始聊天

### 命令系统
所有命令都以 `#` 开头，参数用空格分隔：

| 命令 | 功能 | 用法示例 |
|------|------|----------|
| `#help` | 显示帮助信息 | `#help` |
| `#packet` | 发送红包 | `#packet 5 100 新年快乐` |
| `#revoke` | 撤回最后一条消息 | `#revoke` |
| `#exit` | 退出登录 | `#exit` |
| `#web` | 切换显示模式 | `#web 1` (开启) / `#web 0` (关闭) |
| `#clear` | 清空聊天记录 | `#clear` |
| `#eventLog` | 事件日志开关 | `#eventLog 1` |
| `#openmsg` | 红包消息提醒开关 | `#openmsg 0` |
| `#auto_packet` | 自动抢红包开关 | `#auto_packet 1` |

### 快捷操作
- **发送消息**: <kbd>Enter</kbd>
- **换行**: <kbd>Shift</kbd> + <kbd>Enter</kbd>
- **历史消息**: <kbd>↑</kbd> / <kbd>↓</kbd>
- **@用户**: 双击用户列表中的用户名

## 🔧 系统要求

### IDE兼容性
- **支持版本**: IntelliJ IDEA 2023.1 - 2024.3
- **操作系统**: Windows / macOS / Linux
- **网络**: 需要能够访问 fishpi.cn

### 🔥 重要说明：JDK版本兼容性

**✅ 对老用户完全兼容！**

- **用户项目JDK**: 支持 **Java 8** 及以上版本
- **IDE内置运行时**: IDEA自带JetBrains Runtime，无需用户安装
- **插件构建**: 使用Java 11编译，确保稳定性

**📝 详细说明**:
1. **插件编译版本** ≠ **用户项目JDK版本**
2. 即使插件用Java 11编译，用户仍可使用Java 8开发项目
3. IntelliJ IDEA 2023.1-2024.3均支持Java 8项目开发
4. 插件运行在IDEA的JVM中，与用户项目JDK独立

## 🛠️ 技术架构

本插件基于以下技术构建：

- **语言**: Kotlin 1.8.22
- **框架**: IntelliJ Platform Plugin SDK
- **网络**: OkHttp4 + WebSocket
- **UI**: Swing + JCEF (Web模式)
- **数据解析**: Gson
- **构建工具**: Gradle
- **编译目标**: Java 11 (向下兼容Java 8用户)

## 📝 版本历史

### v1.0.0 (当前版本)
- 🎉 重大更新：品牌重命名为 FishPi Chat
- ✅ 兼容性：支持 IntelliJ IDEA 2023.1 - 2024.3
- 🔧 技术升级：升级到 Java 11、Kotlin 1.8.22
- 📦 依赖更新：更新所有核心依赖库到稳定版本
- 🐛 修复兼容性问题
- ✅ **保持Java 8项目开发兼容性**

### v0.3.1 (旧版本)
- 新增 WebSocket URL 动态获取
- 优化连接稳定性

### v0.3.0
- 添加客户端标识
- 改进消息显示

### v0.2.0
- Web视图记录数量限制（200条）
- 活跃度进度条实时更新
- 修复Web视图点歌卡死问题

### v0.1.8
- 新增自动抢红包控制开关

## 🔄 迁移指南

如果您之前使用的是 PWL Chat 插件，请注意：

1. **插件名称变更**: PWL Chat → FishPi Chat
2. **工具窗口**: 底部面板从 `PWL` 更名为 `FishPi`
3. **兼容性提升**: 新版本支持更广泛的 IDEA 版本
4. **功能保持**: 所有原有功能均保持不变
5. **JDK兼容**: **继续支持Java 8用户项目开发**

## ❓ 常见问题

### Q: 我还在用Java 8开发项目，能使用这个插件吗？
**A: 完全可以！** 插件使用Java 11编译不影响您使用Java 8开发项目。IDEA支持Java 8项目开发到2024.3版本。

### Q: 为什么插件要用Java 11编译？
**A: 为了稳定性和安全性**。使用Java 11编译能获得更好的性能和安全特性，但不影响用户项目的JDK版本选择。

### Q: 插件更新后我的Java 8项目还能正常工作吗？
**A: 绝对可以！** 插件运行在IDEA的JVM中，与您的项目JDK完全独立。

## 🤝 参与贡献

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开 Pull Request

## 📞 联系方式

- **作者**: DanBai
- **邮箱**: danbai@88.com
- **个人网站**: https://p00q.cn
- **社区**: [摸鱼派](https://fishpi.cn)

## 📄 开源协议

本项目基于 [IntelliJ Platform Plugin Template](https://github.com/JetBrains/intellij-platform-plugin-template) 开发。

## 🙏 鸣谢

- [摸鱼派社区](https://fishpi.cn) - 提供优秀的交流平台
- [JetBrains](https://www.jetbrains.com/) - 提供强大的IDE开发平台
- 所有为本项目贡献代码和建议的开发者们

---

**开发不易，如果这个插件对你有帮助，欢迎到摸鱼派社区支持一下！** 🎉
