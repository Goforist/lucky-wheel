# GitHub Pages 部署指南

按照以下步骤将转盘应用部署到 GitHub Pages：

## 第一步：在 GitHub 上创建仓库

1. 访问 [GitHub](https://github.com) 并登录（如果没有账号，先注册）
2. 点击右上角的 **"+"** 按钮，选择 **"New repository"**
3. 填写仓库信息：
   - **Repository name**: `lucky-wheel`（或你喜欢的名字）
   - **Description**: 幸运转盘应用（可选）
   - **选择 Public**（公开，这样才能使用免费的 GitHub Pages）
   - **不要**勾选 "Initialize this repository with a README"（我们已经有了文件）
4. 点击 **"Create repository"**

## 第二步：将代码推送到 GitHub

在终端中执行以下命令（我已经帮你初始化了 git 仓库）：

```bash
# 1. 添加所有文件
git add .

# 2. 创建初始提交
git commit -m "Initial commit: 幸运转盘应用"

# 3. 添加远程仓库（将 YOUR_USERNAME 替换为你的 GitHub 用户名）
git remote add origin https://github.com/YOUR_USERNAME/lucky-wheel.git

# 4. 将代码推送到 GitHub
git branch -M main
git push -u origin main
```

**注意**：执行第 3 步时，需要将 `YOUR_USERNAME` 替换为你的实际 GitHub 用户名，`lucky-wheel` 替换为你创建的仓库名。

如果 GitHub 要求身份验证，你可能需要：
- 使用 Personal Access Token（推荐）
- 或者使用 GitHub CLI

## 第三步：启用 GitHub Pages

1. 在 GitHub 仓库页面，点击 **"Settings"**（设置）标签
2. 在左侧菜单中找到并点击 **"Pages"**
3. 在 **"Source"** 部分：
   - 选择 **"Deploy from a branch"**
   - Branch 选择 **"main"**
   - Folder 选择 **"/ (root)"**
4. 点击 **"Save"** 按钮
5. 等待几分钟（通常 1-2 分钟），GitHub 会生成你的网站链接

## 第四步：访问和分享

1. 在 Settings → Pages 页面，你会看到你的网站链接，格式如：
   ```
   https://YOUR_USERNAME.github.io/lucky-wheel/
   ```
2. 点击这个链接，你的转盘应用就可以在线访问了！
3. 将这个链接分享给任何人，他们都可以使用你的转盘应用

## 后续更新

如果以后修改了代码，只需要：

```bash
git add .
git commit -m "更新说明"
git push
```

GitHub Pages 会自动更新（通常需要几分钟）。

## 常见问题

### Q: 如果推送时要求输入用户名和密码？
A: GitHub 现在要求使用 Personal Access Token 而不是密码。可以：
- 访问 https://github.com/settings/tokens
- 生成新的 token（选择 repo 权限）
- 使用 token 作为密码

### Q: 网站链接显示 404？
A: 等待几分钟，GitHub Pages 需要时间构建。如果超过 10 分钟还是 404，检查：
- 仓库是否为 Public
- index.html 是否在根目录
- Pages 设置是否正确

### Q: 如何自定义域名？
A: 在 Settings → Pages 中可以设置 Custom domain。

---

**需要帮助？** 如果遇到问题，告诉我具体的错误信息，我会帮你解决！

