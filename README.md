# 🎮 Unity 通用自动化构建系统

> 🚀 一个轻量级、可扩展的Unity项目自动化构建系统，支持多项目、多平台的构建需求。

## ✨ 主要特性

| 特性 | 描述 |
|------|------|
| 🌍 多平台支持 | Android、iOS、PC等全平台支持 |
| 🔄 自动化集成 | 无缝集成GitHub Actions |
| 📦 统一构建流程 | 标准化的构建流程和配置 |
| 📊 实时监控 | 构建状态和性能实时监控 |
| 🛠️ 高度可定制 | 灵活的构建参数配置 |
| 📝 完整日志 | 详细的构建记录追踪 |
| 🔒 安全管理 | 证书和密钥安全存储 |
| ⚡ 增量构建 | 智能构建缓存机制 |
| 📈 性能优化 | 构建性能持续优化 |
| 🔄 并行构建 | 多平台并行构建支持 |

## 💻 快速开始

> 📖 查看我们的[快速开始指南](QUICK_START.md)，5分钟内完成系统配置！

### ⚡️ 三步上手

1️⃣ **添加构建系统**
```bash
git submodule add https://github.com/Tianyuyuyuyuyuyu/UnityBuild.git BuildSystem
```

2️⃣ **配置项目**
```yaml
# build-config.yml
project_name: "YourProject"
unity_version: "2021.3.1f1"
build_targets:
  - Android
  - iOS
```

3️⃣ **配置环境变量**

| 变量类型 | 变量名 | 说明 |
|---------|--------|------|
| 必需 | `UNITY_LICENSE` | Unity许可证内容 |
| 必需 | `UNITY_EMAIL` | Unity账号邮箱 |
| 必需 | `UNITY_PASSWORD` | Unity账号密码 |
| 可选 | `UNITY_SERIAL` | Unity序列号 |
| 可选 | `ANDROID_KEYSTORE_BASE64` | Android签名文件 |

> 🎯 更多详细配置和高级用法，请查看[快速开始指南](QUICK_START.md)！

## 💻 系统要求

### 🖥️ 构建服务器要求
| 要求 | 规格 |
|------|------|
| 系统 | Ubuntu 22.04 LTS |
| 内存 | ≥ 8GB |
| CPU | ≥ 4核 |
| 存储 | ≥ 50GB可用空间 |
| 网络 | 可访问GitHub和Unity服务器 |

### 🎮 Unity要求
- ✅ Unity 2020.3或更高版本
- ✅ Unity Build Support模块：
  - 📱 Android Build Support
  - 🍎 iOS Build Support
  - 🌐 WebGL Build Support（可选）
- ✅ Unity许可证（Personal/Professional/Enterprise）

### 🛠️ 其他要求
- 📌 Git 2.x或更高版本
- 📌 GitHub账号和仓库
- 📌 Unity账号

## 📁 目录结构

```
unity-build-system/
├── 📂 .github/
│   └── 📂 workflows/          # GitHub Actions工作流
├── 📂 scripts/
│   ├── 📂 build/             # 核心构建脚本
│   └── 📂 utils/             # 工具脚本
├── 📂 configs/               # 配置文件
├── 📂 docs/                 # 文档
└── 📂 tests/               # 测试用例
```

## 🚀 快速开始

### 1️⃣ 添加构建系统

```bash
git submodule add https://github.com/Tianyuyuyuyuyuyu/UnityBuild.git BuildSystem
```

### 2️⃣ 配置项目

```yaml
# build-config.yml
project_name: "YourProject"
unity_version: "2021.3.1f1"
build_targets:
  - Android
  - iOS
```

### 3️⃣ 环境变量配置

| 变量类型 | 变量名 | 说明 |
|---------|--------|------|
| 必需 | `UNITY_LICENSE` | Unity许可证内容 |
| 必需 | `UNITY_EMAIL` | Unity账号邮箱 |
| 必需 | `UNITY_PASSWORD` | Unity账号密码 |
| 可选 | `UNITY_SERIAL` | Unity序列号 |
| 可选 | `ANDROID_KEYSTORE_BASE64` | Android签名文件 |

## ⚙️ 配置说明

### 📱 平台特定配置

<details>
<summary>Android配置</summary>

```yaml
android:
  target_sdk: 33
  min_sdk: 24
  bundle: true
  signing: true
```
</details>

<details>
<summary>iOS配置</summary>

```yaml
ios:
  target_sdk: latest
  signing_team_id: "XXXXXXXX"
```
</details>

## 🔧 性能优化建议

### 🚀 构建速度优化
- 💾 使用构建缓存
- ⚡ 启用增量构建
- 📦 优化资源导入
- 💫 使用SSD存储

### 📦 资源优化
- 🎯 使用Asset Bundle
- 🗜️ 压缩构建产物
- 🧹 清理未使用资源

## 🔒 安全建议

- 🔑 使用GitHub Secrets存储敏感信息
- 🔄 定期轮换密钥
- 👥 严格的访问控制
- 📝 安全日志记录

## 🤝 贡献指南

1. 🍴 Fork 项目
2. 🌿 创建特性分支
3. 📝 提交更改
4. 🚀 推送到分支
5. 📫 创建 Pull Request

## 📄 许可证

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 👨‍💻 维护者

[![GitHub](https://img.shields.io/github/followers/Tianyuyuyuyuyuyu?style=social)](https://github.com/Tianyuyuyuyuyuyu)

## 🗺️ 路线图

- [ ] 🌟 支持更多构建平台
- [ ] ⚡ 优化构建性能
- [ ] 🎨 添加更多自定义选项
- [ ] 📊 改进监控系统
- [ ] 🧪 集成测试框架

## 📞 联系方式

[![Issues](https://img.shields.io/github/issues/Tianyuyuyuyuyuyu/UnityBuild)](https://github.com/Tianyuyuyuyuyuyu/UnityBuild/issues)
[![Email](https://img.shields.io/badge/Email-tianyulovecars%40gmail.com-blue)](mailto:tianyulovecars@gmail.com)

## 🙏 致谢

感谢所有为这个项目做出贡献的开发者。

## 📚 相关资源

[![Unity](https://img.shields.io/badge/Unity-Documentation-black)](https://docs.unity3d.com/Manual/CommandLineArguments.html)
[![GitHub Actions](https://img.shields.io/badge/GitHub-Actions-2088FF)](https://docs.github.com/en/actions)
[![Cloud Build](https://img.shields.io/badge/Unity-Cloud%20Build-green)](https://unity.com/products/cloud-build)