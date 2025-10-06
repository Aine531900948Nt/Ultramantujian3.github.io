# 部署指南

## GitHub Pages 部署步骤

### 1. 准备工作
- 确保所有文件都在项目根目录
- index.html 作为入口文件
- 配置 Bmob 后端服务

### 2. 创建 GitHub 仓库
1. 在 GitHub 创建新仓库（如：ultraman-guide）
2. 将所有项目文件推送到仓库

```bash
git init
git add .
git commit -m "Initial commit: Ultraman Guide Complete"
git branch -M main
git remote add origin https://github.com/your-username/ultraman-guide.git
git push -u origin main
```

### 3. 启用 GitHub Pages
1. 进入仓库 Settings
2. 找到 Pages 选项
3. 选择 Source: Deploy from a branch
4. 选择 Branch: main / (root)
5. 点击 Save

### 4. 配置 Bmob 安全域名
1. 登录 Bmob 控制台
2. 进入应用设置 > 安全设置 > 安全域名
3. 添加您的 GitHub Pages 域名：
   - https://your-username.github.io
   - https://your-username.github.io/ultraman-guide

### 5. 更新配置文件
编辑 `js/bmob-config.js`，替换：
- YOUR_BMOB_APP_ID
- YOUR_BMOB_REST_API_KEY

### 6. 测试功能
部署完成后，访问您的 GitHub Pages 链接测试：
- 页面加载和导航
- 搜索功能
- 收藏系统
- 开发者模式（密码：11111111）

## 本地测试

### 使用 Live Server (VS Code 插件)
1. 安装 Live Server 插件
2. 右键 index.html
3. 选择 "Open with Live Server"

### 使用 Python (如果可用)
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

### 使用 Node.js (如果可用)
```bash
npx serve . -p 8000
```

### 直接在浏览器中打开
注意：某些功能可能因为 CORS 限制而无法正常工作。

## 功能测试清单

### ✅ 基础功能
- [ ] 页面正常加载
- [ ] 导航栏工作正常
- [ ] 响应式设计适配不同屏幕

### ✅ 数据功能
- [ ] Bmob 连接正常
- [ ] 数据服务工作
- [ ] 错误处理正确

### ✅ 核心模块
- [ ] 搜索功能正常
- [ ] 筛选功能工作
- [ ] 收藏系统可用
- [ ] 对比功能正常
- [ ] 时间轴显示正确

### ✅ 开发者功能
- [ ] 登录验证正常
- [ ] 数据管理功能
- [ ] 图片上传功能
- [ ] 导入/导出功能

## 常见问题

### Q: 页面显示配置错误
A: 检查 bmob-config.js 中的 APP_ID 和 REST_API_KEY 配置

### Q: 图片上传失败
A: 确保 Bmob 安全域名配置正确

### Q: 搜索无结果
A: 检查数据库中是否有数据，或使用开发者模式添加测试数据

### Q: 收藏功能异常
A: 检查浏览器是否支持 localStorage

## 性能优化建议

1. **图片优化**
   - 使用 WebP 格式
   - 压缩图片大小
   - 添加懒加载

2. **代码优化**
   - 压缩 CSS/JS 文件
   - 启用 Gzip 压缩
   - 使用 CDN 加速

3. **缓存策略**
   - 设置适当的缓存头
   - 使用浏览器缓存
   - 实现离线缓存

## 后续升级

1. **添加新功能**
   - 用户系统
   - 评论功能
   - 社交分享

2. **技术升级**
   - PWA 支持
   - 离线功能
   - 推送通知

3. **数据扩展**
   - 更多角色数据
   - 视频内容
   - 3D 模型展示