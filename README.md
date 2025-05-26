# ComfyNode Preview

一个用于预览ComfyUI工作流的在线工具。

## 功能特性

- 🖼️ 支持拖拽上传ComfyUI工作流文件（JSON格式）
- 🎨 支持从PNG图片中提取工作流信息
- 📊 可视化展示节点关系图
- 📱 响应式设计，支持移动端
- 💾 本地历史记录功能

## 在线使用

访问：[ComfyNode Preview](https://你的用户名.github.io/node_preview)

## 本地使用

1. 克隆仓库：
```bash
git clone https://github.com/你的用户名/node_preview.git
```

2. 在本地服务器中打开：
```bash
# 使用Python
python -m http.server 8000

# 或使用Node.js
npx serve .
```

3. 在浏览器中访问 `http://localhost:8000`

## 使用方法

1. 将ComfyUI的工作流JSON文件或包含工作流信息的PNG图片拖拽到页面中
2. 系统会自动解析并展示节点关系图
3. 可以缩放和拖拽查看工作流的详细结构

## 技术栈

- HTML5
- CSS3
- JavaScript (ES6+)
- LiteGraph.js - 用于图形渲染
- EXIF.js - 用于PNG图片元数据提取

## 贡献

欢迎提交Issue和Pull Request！

## 许可证

MIT License 