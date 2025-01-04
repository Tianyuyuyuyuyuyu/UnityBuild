# Unity构建系统快速开始指南

## 📝 前置要求

在开始之前，请确保你的环境满足以下要求：

- ✅ 已安装Git
- ✅ 已安装Unity（2020.3或更高版本）
- ✅ 有GitHub账号
- ✅ 有Unity账号和许可证

## 🚀 快速开始

### 1. 准备你的Unity项目

#### 1.1 如果你已经有Git仓库的Unity项目
确认你的项目根目录下有 `.git` 目录，如果有，可以直接进行下一步。

#### 1.2 如果你的Unity项目还没有使用Git
```bash
# 进入你的Unity项目根目录
cd 你的Unity项目路径

# 初始化Git仓库
git init

# 添加所有文件到Git
git add .

# 创建首次提交
git commit -m "初始化Unity项目"
```

### 2. 项目结构示例

在添加构建系统之前，你的Unity项目结构可能是这样的：
```
你的Unity项目/
├── Assets/
├── Packages/
├── ProjectSettings/
└── ...其他Unity文件和目录
```

### 3. 添加构建系统

在项目根目录执行以下命令：
```bash
# 添加构建系统作为子模块
git submodule add https://github.com/Tianyuyuyuyuyuyu/UnityBuild.git BuildSystem
```

添加后，你的项目结构会变成这样：
```
你的Unity项目/
├── Assets/
├── Packages/
├── ProjectSettings/
├── BuildSystem/        <-- 新添加的构建系统
│   ├── scripts/
│   ├── configs/
│   └── ...构建系统的其他文件
├── .gitmodules        <-- 新添加的子模块配置文件
└── ...其他Unity文件和目录
```

### 4. 配置构建参数

在项目根目录创建 `build-config.yml` 文件：
```yaml
project_name: "你的项目名"
unity_version: "2021.3.1f1"  # 使用你的Unity版本
build_targets:
  - Android
  - iOS
```

### 5. 配置GitHub仓库

1. 在GitHub上创建仓库（如果还没有）
2. 添加必要的密钥（在仓库的Settings > Secrets and variables > Actions中）：
   - `UNITY_LICENSE`：Unity许可证内容
   - `UNITY_EMAIL`：Unity账号邮箱
   - `UNITY_PASSWORD`：Unity账号密码
   - `ANDROID_KEYSTORE_BASE64`：（如需Android构建）

### 6. 日常使用说明

#### 6.1 克隆带有构建系统的项目
```bash
# 克隆你的项目
git clone 你的项目地址

# 初始化并更新子模块
git submodule init
git submodule update
```

#### 6.2 更新构建系统
```bash
# 更新构建系统到最新版本
cd BuildSystem
git pull origin main
cd ..
```

## ⚠️ 注意事项

1. **子模块管理**
   - 子模块是独立的Git仓库
   - 更新子模块需要单独进行
   - 团队成员需要了解子模块的基本操作

2. **构建配置**
   - 确保 `build-config.yml` 中的Unity版本与项目一致
   - 正确配置构建目标平台
   - 妥善保管各类密钥和证书

3. **常见问题解决**
   - 如果子模块更新失败，检查网络连接
   - 确保GitHub Actions权限配置正确
   - 查看构建日志排查问题

## 🔍 帮助和支持

如果你在使用过程中遇到问题：
1. 查看构建系统的详细文档
2. 检查GitHub Actions的构建日志
3. 通过Issues反馈问题
4. 联系技术支持团队

## 📚 相关资源

- [Unity文档](https://docs.unity3d.com)
- [GitHub Actions文档](https://docs.github.com/en/actions)
- [Git子模块文档](https://git-scm.com/book/en/v2/Git-Tools-Submodules) 