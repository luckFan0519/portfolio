# 姜凡个人主页

云南大学智能科学与技术本科生个人作品集页面。

## 在线访问

部署后访问：`https://luckfan0519.github.io/`

## 部署到 GitHub Pages（详细步骤）

### 方法一：创建 username.github.io 仓库（推荐）

1. **在 GitHub 上创建仓库**
   - 登录 GitHub，点击右上角 `+` → `New repository`
   - 仓库名填：`luckFan0519.github.io`（必须和你的用户名一致）
   - 选择 `Public`
   - 勾选 `Add a README file`
   - 点击 `Create repository`

2. **上传文件**
   - 将 `portfolio` 文件夹中的所有文件上传到仓库根目录
   - 可以用 GitHub 网页端直接拖拽上传，也可以用 Git 命令：

   ```powershell
   # 进入 portfolio 目录
   cd portfolio

   # 初始化 Git 仓库
   git init

   # 添加所有文件
   git add .

   # 提交
   git commit -m "Initial commit: personal portfolio"

   # 关联远程仓库
   git remote add origin https://github.com/luckFan0519/luckFan0519.github.io.git

   # 推送
   git branch -M main
   git push -u origin main
   ```

3. **开启 GitHub Pages**
   - 进入仓库 → `Settings` → `Pages`
   - `Source` 选择 `Deploy from a branch`
   - `Branch` 选择 `main`，文件夹选择 `/ (root)`
   - 点击 `Save`
   - 等待 1-2 分钟，访问 `https://luckfan0519.github.io/` 即可看到页面

### 方法二：放到现有仓库的 gh-pages 分支

如果已有同名仓库 `luckFan0519.github.io`，可以将文件推送到 `gh-pages` 分支：

```powershell
cd portfolio
git init
git add .
git commit -m "Add portfolio"
git branch -M gh-pages
git remote add origin https://github.com/luckFan0519/luckFan0519.github.io.git
git push -u origin gh-pages
```

然后在仓库 `Settings` → `Pages` 中将 Branch 设为 `gh-pages`。

## 本地预览

直接用浏览器打开 `index.html` 即可预览。

或使用本地服务器：

```powershell
# Python
python -m http.server 8080

# 然后访问 http://localhost:8080
```

## 项目结构

```
portfolio/
├── index.html              # 主页面
├── assets/
│   ├── css/style.css       # 样式文件
│   ├── js/main.js          # 交互脚本
│   └── images/             # 图片资源
└── README.md
```

## 技术栈

- HTML5 / CSS3 / Vanilla JavaScript
- Canvas 粒子背景
- IntersectionObserver 滚动动画
- CSS Glassmorphism 玻璃拟态
- 3D Tilt 卡片效果

## License

个人使用，请勿用于商业用途。
