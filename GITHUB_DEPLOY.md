# 矿工星火助手 - GitHub Pages 部署指南

本指南将帮助您将矿工星火星火助手项目部署到GitHub Pages，使其可以通过互联网访问。

## 前提条件

- 已安装Git
- 拥有GitHub账号
- 对Git基本操作有了解

## 部署步骤

### 1. 创建GitHub仓库

1. 登录您的GitHub账号
2. 点击右上角的"+"图标，选择"New repository"
3. 填写仓库信息：
   - Repository name: 建议使用 `miner-assistant` 或其他您喜欢的名称
   - Description: 可选，例如 "矿工星火助手 - 一站式矿工辅助平台"
   - 选择 "Public" (公开仓库)
   - 勾选 "Add a README file"
   - 点击 "Create repository"

### 2. 准备本地项目

确保您的本地项目结构如下：

```
miner_assistant/
├── index.html          # 主页面
├── formation-diagram.html  # 阵法图计算器页面
├── test-animation.html     # 动画测试页面
├── README.md           # 项目说明
└── GITHUB_DEPLOY.md    # 本部署指南
```

### 3. 初始化Git仓库并提交代码

打开终端，导航到您的项目目录：

```bash
cd /path/to/miner_assistant
```

初始化Git仓库：

```bash
git init
```

添加所有文件：

```bash
git add .
```

提交代码：

```bash
git commit -m "Initial commit: 矿工星火助手项目"
```

### 4. 关联GitHub远程仓库

复制您在GitHub上创建的仓库的URL（HTTPS或SSH），例如：

```bash
git remote add origin https://github.com/yourusername/miner-assistant.git
```

### 5. 推送到GitHub

```bash
git push -u origin main
```

如果您使用的是SSH且遇到权限问题，请确保您的SSH密钥已添加到GitHub账号。

### 6. 配置GitHub Pages

1. 进入您的GitHub仓库页面
2. 点击顶部的 "Settings" 选项卡
3. 在左侧导航栏中找到并点击 "Pages"
4. 在 "Source" 部分：
   - 从下拉菜单中选择分支：`main`
   - 选择文件夹：`/(root)` (根目录)
   - 点击 "Save"
5. 等待几分钟，GitHub Pages将为您的项目构建并部署

### 7. 访问您的网站

部署完成后，您可以通过以下URL访问您的网站：

```
https://yourusername.github.io/miner-assistant/
```

其中 `yourusername` 是您的GitHub用户名。

## 后续更新

当您对项目进行修改后，只需执行以下命令即可更新GitHub Pages：

```bash
git add .
git commit -m "描述您的更新内容"
git push origin main
```

GitHub Pages将自动重新构建您的网站，通常需要几分钟时间生效。

## 常见问题

### 1. 页面加载后样式错乱或JavaScript不工作

- 检查文件路径是否正确，确保所有CSS和JavaScript文件都能被正确引用
- 确保您的HTML文件中的所有外部资源链接正确

### 2. 部署后看不到最新更改

- GitHub Pages可能需要几分钟时间更新
- 尝试清除浏览器缓存或使用无痕模式访问

### 3. 404错误

- 确保您选择了正确的分支和文件夹
- 检查文件名是否正确（区分大小写）

## 自定义域名（可选）

如果您拥有自己的域名，可以将其绑定到GitHub Pages：

1. 在您的域名提供商处添加CNAME记录，指向 `yourusername.github.io`
2. 在GitHub仓库的根目录创建一个名为 `CNAME` 的文件，内容为您的域名（例如 `miner-assistant.example.com`）
3. 提交并推送该文件
4. 在GitHub Pages设置中，输入您的自定义域名并保存

## 总结

通过以上步骤，您已经成功将矿工星火助手项目部署到GitHub Pages。现在您可以与他人分享您的网站链接，他们可以在任何设备上访问和使用这个项目。

如需进一步帮助，请参考GitHub官方文档：[GitHub Pages文档](https://docs.github.com/en/pages)
