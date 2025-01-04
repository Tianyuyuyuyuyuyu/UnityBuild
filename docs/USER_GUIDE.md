# Unity构建系统使用指南

## 快速开始 🚀

### 基础使用（适合小型项目）

1. **添加构建系统**
```bash
git submodule add https://github.com/Tianyuyuyuyuyuyu/UnityBuild.git BuildSystem
```

2. **创建配置文件**
在项目根目录创建 `build-config.yml`：
```yaml
mode: "simple"
project_name: "YourProject"
unity_version: "2021.3.1f1"
```

3. **设置GitHub Secrets**
在你的GitHub仓库设置中添加以下secrets：
- UNITY_LICENSE
- UNITY_EMAIL
- UNITY_PASSWORD

4. **开始使用**
- 推送代码到GitHub
- 在Actions页面查看构建状态
- 在Releases页面获取构建产物

### 进阶使用（适合中大型项目）

如果你需要更多构建次数或更强大的功能：

1. **升级配置**
```yaml
mode: "professional"
project_name: "YourProject"
unity_version: "2021.3.1f1"
server_config:
  enabled: true
  url: "${SERVER_URL}"
  credentials: "${SERVER_CREDENTIALS}"
```

2. **运行配置助手**
```bash
./setup.sh --mode professional
```

## 功能对比 📊

| 功能 | 基础模式 | 进阶模式 |
|------|----------|----------|
| 基础构建 | ✅ | ✅ |
| 自动版本管理 | ✅ | ✅ |
| 基础缓存 | ✅ | ✅ |
| 高级缓存 | ❌ | ✅ |
| 无限构建次数 | ❌ | ✅ |
| 自动负载均衡 | ❌ | ✅ |

## 常见问题 ❓

### 如何获取Unity许可证？
1. 登录Unity账号
2. 访问许可证管理页面
3. 生成新的许可证
4. 复制许可证内容到GitHub Secrets

### 构建失败怎么办？
1. 检查Unity版本是否匹配
2. 确认Secrets配置是否正确
3. 查看构建日志了解详细错误

### 如何自定义构建流程？
1. 修改 `build-config.yml`
2. 添加自定义构建步骤
3. 配置构建参数

## 获取帮助 💡

- 查看详细文档：[文档中心](./docs)
- 提交Issue：[问题反馈](https://github.com/Tianyuyuyuyuyuyu/UnityBuild/issues)
- 加入社区：[Discord](your-discord-link)

## 最佳实践 ⭐

1. **配置管理**
   - 使用版本控制管理配置
   - 区分开发和生产环境
   - 定期更新构建系统

2. **性能优化**
   - 使用构建缓存
   - 清理未使用资源
   - 合理设置构建参数

3. **团队协作**
   - 统一构建配置
   - 规范分支管理
   - 及时同步更新 