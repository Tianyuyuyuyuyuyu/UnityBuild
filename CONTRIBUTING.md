# 贡献指南

> 🎮 感谢你考虑为 Unity 通用自动化构建系统做出贡献！

## 📋 目录

- [行为准则](#行为准则)
- [开始贡献](#开始贡献)
- [开发流程](#开发流程)
- [提交指南](#提交指南)
- [分支管理](#分支管理)
- [代码规范](#代码规范)
- [文档规范](#文档规范)
- [测试规范](#测试规范)
- [版本发布](#版本发布)

## 📜 行为准则

本项目采用 [Contributor Covenant](https://www.contributor-covenant.org/version/2/0/code_of_conduct/) 行为准则。参与本项目即表示您同意遵守其条款。

## 🚀 开始贡献

### 1. 准备工作

- Fork 本仓库
- 克隆你的 Fork 仓库到本地
- 设置上游仓库

```bash
# 克隆你的 Fork 仓库
git clone https://github.com/你的用户名/UnityBuild.git

# 添加上游仓库
git remote add upstream https://github.com/Tianyuyuyuyuyuyu/UnityBuild.git
```

### 2. 创建工作分支

```bash
# 更新主分支
git checkout main
git pull upstream main

# 创建新分支
git checkout -b feature/your-feature-name
```

## 💻 开发流程

1. **选择任务**
   - 查看 [Issues](https://github.com/Tianyuyuyuyuyuyu/UnityBuild/issues) 列表
   - 在相关 Issue 下留言表明你要处理该任务
   - 如果是新功能，请先创建 Issue 讨论

2. **本地开发**
   - 遵循代码规范
   - 编写必要的测试
   - 确保所有测试通过
   - 更新相关文档

3. **提交变更**
   - 遵循提交信息规范
   - 确保每个提交都是独立且完整的
   - 在提交信息中引用相关的 Issue

## 📝 提交指南

### 提交信息格式

```
<类型>(<范围>): <描述>

[可选的正文]

[可选的脚注]
```

### 类型

- `feat`: 新功能
- `fix`: 修复
- `docs`: 文档更新
- `style`: 代码格式（不影响代码运行的变动）
- `refactor`: 重构（既不是新增功能，也不是修改bug的代码变动）
- `perf`: 性能优化
- `test`: 增加测试
- `chore`: 构建过程或辅助工具的变动

### 示例

```
feat(android): 添加Android自动签名功能

- 实现自动读取keystore文件
- 添加签名配置验证
- 更新相关文档

Closes #123
```

## 🌿 分支管理

- `main`: 主分支，保持稳定
- `develop`: 开发分支
- `feature/*`: 功能分支
- `fix/*`: 修复分支
- `release/*`: 发布分支

## 📐 代码规范

### C# 代码规范

- 使用 [Microsoft C# 编码约定](https://docs.microsoft.com/zh-cn/dotnet/csharp/fundamentals/coding-style/coding-conventions)
- 类名使用 PascalCase
- 方法名使用 PascalCase
- 变量名使用 camelCase
- 常量使用 UPPER_CASE
- 使用有意义的命名
- 添加必要的注释

### Unity 相关规范

- 场景命名使用 PascalCase
- 预制体命名使用 PascalCase
- 资源文件使用小写和连字符
- 遵循 Unity 官方的最佳实践

## 📚 文档规范

- 使用 Markdown 格式
- 文档应清晰易读
- 包含必要的示例
- 保持文档与代码同步更新
- 使用适当的标题层级
- 添加必要的链接和引用

## ✅ 测试规范

### 单元测试

- 每个功能都应有对应的单元测试
- 测试应该独立且可重复
- 使用有意义的测试名称
- 遵循 AAA (Arrange-Act-Assert) 模式

### 集成测试

- 确保主要功能流程的集成测试覆盖
- 模拟真实使用场景
- 处理异常情况

## 📦 版本发布

### 版本号规范

遵循 [语义化版本 2.0.0](https://semver.org/lang/zh-CN/)：

- 主版本号：不兼容的 API 修改
- 次版本号：向下兼容的功能性新增
- 修订号：向下兼容的问题修正

### 发布流程

1. 更新版本号
2. 更新 CHANGELOG.md
3. 创建发布分支
4. 进行发布测试
5. 合并到主分支
6. 创建发布标签

## 🤝 贡献者

感谢所有贡献者的付出！

[![贡献者](https://contrib.rocks/image?repo=Tianyuyuyuyuyuyu/UnityBuild)](https://github.com/Tianyuyuyuyuyuyu/UnityBuild/graphs/contributors)

## ❓ 获取帮助

- 查看 [文档](./docs)
- 提交 [Issue](https://github.com/Tianyuyuyuyuyuyu/UnityBuild/issues)
- 发送邮件至 [tianyulovecars@gmail.com](mailto:tianyulovecars@gmail.com)

---

再次感谢您的贡献！🎮✨ 