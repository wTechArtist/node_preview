# GitHub Pages 部署指南

## 方法一：Fork 原仓库并启用 GitHub Pages（推荐）

1. **Fork 仓库**
   - 访问 https://github.com/wTechArtist/node_preview
   - 点击右上角的 "Fork" 按钮
   - 选择你的GitHub账户

2. **启用 GitHub Pages**
   - 进入你Fork的仓库
   - 点击 "Settings" 标签页
   - 在左侧菜单中找到 "Pages"
   - 在 "Source" 部分选择 "Deploy from a branch"
   - 选择 "main" 分支和 "/ (root)" 文件夹
   - 点击 "Save"

3. **访问你的网站**
   - GitHub会自动构建并部署
   - 几分钟后，你就可以通过 `https://你的用户名.github.io/node_preview` 访问网站

## 方法二：创建新仓库并使用 GitHub Actions

1. **创建新的GitHub仓库**
   - 登录GitHub，创建新仓库
   - 仓库名建议使用 `node_preview` 或 `comfyui-workflow-preview`
   - 设置为Public（GitHub Pages需要）

2. **上传代码**
   ```bash
   # 如果还没有，先克隆原仓库
   git clone https://github.com/wTechArtist/node_preview.git
   cd node_preview
   
   # 更改远程仓库地址
   git remote set-url origin https://github.com/你的用户名/你的仓库名.git
   
   # 推送到你的仓库
   git add .
   git commit -m "Initial commit"
   git push -u origin main
   ```

3. **启用 GitHub Pages**
   - 进入仓库的 Settings → Pages
   - Source 选择 "GitHub Actions"
   - 代码中已包含自动部署的工作流文件

4. **自动部署**
   - 每次推送到main分支时，GitHub Actions会自动构建并部署
   - 查看 Actions 标签页可以看到部署状态

## 自定义域名（可选）

如果你有自己的域名：

1. 在仓库根目录创建 `CNAME` 文件
2. 文件内容写入你的域名，如：`comfyui-preview.yourdomain.com`
3. 在你的域名DNS设置中添加CNAME记录指向：`你的用户名.github.io`

## 注意事项

- GitHub Pages对免费用户有一些限制（如仓库大小、带宽等）
- 部署通常需要几分钟时间
- 如果遇到问题，检查 Actions 页面的构建日志
- 确保仓库是Public的（私有仓库需要付费版GitHub）

## 故障排除

**问题：页面无法加载**
- 检查仓库是否为Public
- 确认GitHub Pages已正确启用
- 查看Actions页面是否有错误

**问题：样式或脚本无法加载**
- 确保所有资源文件路径都是相对路径
- 检查文件名大小写是否正确

**问题：上传功能不工作**
- 这是正常的，GitHub Pages不支持服务器端功能
- 但文件拖拽和前端处理功能都是正常的 