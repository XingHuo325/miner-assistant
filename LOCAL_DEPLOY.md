# 矿工星火助手 - 本地部署指南

本指南将帮助您在本地计算机上运行矿工星火助手项目，无需部署到互联网即可体验所有功能。

## 方法一：直接打开HTML文件（最简单）

这是最简单的方法，适用于快速查看项目。

### 步骤：

1. **找到项目文件**
   - 确保您已经获得了完整的项目文件夹 `miner_assistant`

2. **打开主页面**
   - 找到 `index.html` 文件
   - 双击该文件，它将在您的默认浏览器中打开

3. **浏览功能**
   - 您可以点击各个功能模块图标进入相应页面
   - 阵法图计算器等功能都可以正常使用

### 优点：
- 无需安装任何额外软件
- 操作简单快捷

### 缺点：
- 如果项目中使用了某些高级功能（如fetch、本地存储等），可能会受到浏览器安全限制

## 方法二：使用Python简单HTTP服务器

如果您的电脑上安装了Python，可以使用其内置的HTTP服务器来运行项目。

### 步骤：

1. **安装Python**
   - 如果您还没有安装Python，请从 [python.org](https://www.python.org/) 下载并安装
   - 安装时请勾选 "Add Python to PATH" 选项

2. **打开终端/命令提示符**
   - Windows: 按下 `Win + R`，输入 `cmd` 并回车
   - macOS: 按下 `Command + 空格`，输入 `Terminal` 并回车
   - Linux: 按下 `Ctrl + Alt + T`

3. **导航到项目目录**
   ```bash
   cd /path/to/miner_assistant
   ```
   （将 `/path/to/miner_assistant` 替换为您的项目实际路径）

4. **启动HTTP服务器**
   - Python 3.x:
     ```bash
     python -m http.server 8000
     ```
   - Python 2.x:
     ```bash
     python -m SimpleHTTPServer 8000
     ```

5. **访问项目**
   - 打开浏览器，输入地址：`http://localhost:8000` 或 `http://127.0.0.1:8000`
   - 您将看到项目的主页面

6. **停止服务器**
   - 在终端中按下 `Ctrl + C` 即可停止服务器

### 优点：
- 模拟真实服务器环境
- 避免某些浏览器安全限制
- 无需安装额外软件（如果已安装Python）

### 缺点：
- 需要安装Python
- 需要使用命令行

## 方法三：使用VS Code和Live Server插件

如果您使用Visual Studio Code作为代码编辑器，可以安装Live Server插件来运行项目。

### 步骤：

1. **安装VS Code**
   - 从 [code.visualstudio.com](https://code.visualstudio.com/) 下载并安装VS Code

2. **安装Live Server插件**
   - 打开VS Code
   - 点击左侧导航栏的扩展图标扩展图标（Extensions）
   - 在搜索框中输入 "Live Server"
   - 点击 "Install" 安装该插件

3. **打开项目**
   - 在VS Code中，点击 "File" > "Open Folder"
   - 选择 `miner_assistant` 文件夹

4. **启动Live Server**
   - 右键点击 `index.html` 文件
   - 选择 "Open with Live Server"
   - 项目将在默认浏览器中自动打开

5. **停止服务器**
   - 在VS Code底部状态栏中，点击 "Port: 5500" 旁边的 "Go Live" 按钮
   - 按钮将变为 "Port: 5500"，表示服务器已停止

### 优点：
- 实时预览：修改代码后浏览器自动刷新
- 模拟真实服务器环境
- 界面友好，操作简单

### 缺点：
- 需要安装VS Code和插件
- 占用更多系统资源

## 方法四：使用Node.js和http-server

如果您熟悉Node.js，可以使用http-server包来运行项目。

### 步骤：

1. **安装Node.js**
   - 从 [nodejs.org](https://nodejs.org/) 下载并安装Node.js
   - 安装完成后，npm（Node包管理器）也会自动安装

2. **安装http-server**
   - 打开终端/命令提示符
   - 输入以下命令：
     ```bash
     npm install -g http-server
     ```

3. **导航到项目目录**
   ```bash
   cd /path/to/miner_assistant
   ```

4. **启动服务器**
   ```bash
   http-server -p 8000
   ```

5. **访问项目**
   - 打开浏览器，输入地址：`http://localhost:8000`

6. **停止服务器**
   - 在终端中按下 `Ctrl + C`

### 优点：
- 轻量级且功能强大
- 支持HTTPS等高级功能
- 适合开发环境

### 缺点：
- 需要安装Node.js和额外的包
- 需要使用命令行

## 方法五：使用XAMPP或WAMP（适用于Windows）

如果您需要一个完整的本地服务器环境，可以使用XAMPP或WAMP。

### 步骤（以XAMPP为例）：

1. **下载并安装XAMPP**
   - 从 [apachefriends.org](https://www.apachefriends.org/) 下载XAMPP
   - 运行安装程序，按照提示进行安装

2. **启动Apache服务器**
   - 打开XAMPP控制面板
   - 点击 "Start" 按钮启动Apache服务

3. **复制项目文件**
   - 将 `miner_assistant` 文件夹复制到XAMPP的 `htdocs` 目录下
     - 通常路径为：`C:\xampp\htdocs\`

4. **访问项目**
   - 打开浏览器，输入地址：`http://localhost/miner_assistant`

5. **停止服务器**
   - 在XAMPP控制面板中，点击 "Stop" 按钮停止Apache服务

### 优点：
- 提供完整的Web服务器环境
- 适合开发和测试
- 可以与PHP等后端技术结合使用

### 缺点：
- 安装文件较大
- 配置相对复杂
- 占用更多系统资源

## 推荐方法

根据您的需求，我推荐以下方法：

1. **快速预览**：方法一（直接打开HTML文件）
2. **开发和测试**：方法三（VS Code + Live Server）
3. **简单服务器环境**：方法二（Python HTTP服务器）
4. **完整开发环境**：方法五（XAMPP/WAMP）

## 常见问题解决

### 1. 页面样式错乱或JavaScript不工作

- **检查文件路径**：确保所有CSS和JavaScript文件都能被正确引用
- **使用服务器环境**：如果直接打开HTML文件出现问题，尝试使用方法二或方法三

### 2. 端口被占用

- 如果启动服务器时提示端口已被占用，可以尝试使用其他端口号，例如：
  ```bash
  python -m http.server 8080  # 使用8080端口
  ```
- 然后通过 `http://localhost:8080` 访问

### 3. 浏览器缓存问题

- 如果修改了代码但看不到变化，可能是浏览器缓存导致的
- 尝试按 `Ctrl + Shift + R`（Windows/Linux）或 `Command + Shift + R`（macOS）强制刷新页面

### 4. 跨域资源共享（CORS）问题

- 如果项目中使用了fetch或XMLHttpRequest请求外部资源，可能会遇到CORS问题
- 在本地开发环境中，可以使用浏览器插件或修改服务器配置来解决

## 总结

通过本指南提供的方法，您可以在本地轻松运行矿工星火助手项目。选择最适合您需求的方法，并按照相应步骤操作即可。如果遇到任何问题，请参考常见问题解决部分或查阅相关工具的官方文档。
