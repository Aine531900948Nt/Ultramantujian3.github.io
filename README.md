# 奥特曼图鉴大全

一个功能完整的奥特曼图鉴静态网站，采用纯HTML5、CSS3、JavaScript(ES6+)开发，结合Bootstrap 5实现全端响应式设计。

## 🌟 主要功能

### 📱 核心模块
- **奥特曼图鉴** - 展示奥特曼基础信息、多形态切换、能力雷达图
- **怪兽图鉴** - 怪兽/宇宙人信息展示、分类筛选、能力分析
- **全局搜索** - 支持中/日文名称搜索，智能筛选和高亮显示
- **角色对比** - 2-3个角色参数对比，雷达图叠加展示
- **收藏系统** - 本地收藏管理，支持导入/导出
- **世界观时间轴** - 奥特曼系列历史事件时间轴
- **开发者模式** - 数据管理后台，支持增删改查和图片上传

### 🎨 技术特色
- 📊 **Chart.js雷达图** - 直观展示角色能力数值
- 🌐 **Bmob云存储** - 后端数据存储和图片管理
- 📱 **响应式设计** - 完美适配PC/平板/手机
- 🔄 **PWA特性** - 支持离线访问和本地缓存
- 🎯 **模块化架构** - 清晰的代码结构和组件化设计

## 🚀 快速开始

### 在线访问
访问 GitHub Pages 部署的在线版本：
[https://your-username.github.io/ultraman-guide](https://your-username.github.io/ultraman-guide)

### 本地运行
1. 克隆项目到本地
```bash
git clone https://github.com/your-username/ultraman-guide.git
cd ultraman-guide
```

2. 使用本地HTTP服务器运行
```bash
# 使用Python
python -m http.server 8000

# 或使用Node.js
npx serve .

# 或使用其他HTTP服务器
```

3. 在浏览器中访问 `http://localhost:8000`

## ⚙️ 配置说明

### Bmob后端配置
1. 注册 [Bmob](https://www.bmob.cn/) 账户并创建应用
2. 编辑 `js/bmob-config.js` 文件，替换以下配置：
```javascript
this.APP_ID = 'YOUR_BMOB_APP_ID';
this.REST_API_KEY = 'YOUR_BMOB_REST_API_KEY';
```
3. 在Bmob控制台设置安全域名白名单，添加您的GitHub Pages域名

### 开发者模式
- 默认密码：`11111111`
- 功能：奥特曼/怪兽数据管理、图片上传、系统设置

## 📁 项目结构

```
ultraman-guide/
├── index.html              # 主页面
├── css/
│   └── main.css            # 主样式文件
├── js/
│   ├── bmob-config.js      # Bmob配置
│   ├── data-service.js     # 数据服务层
│   ├── ui-components.js    # UI组件库
│   ├── search.js           # 搜索功能
│   ├── favorites.js        # 收藏系统
│   ├── comparison.js       # 对比功能
│   ├── timeline.js         # 时间轴
│   ├── developer.js        # 开发者模式
│   └── main.js             # 主应用文件
├── images/                 # 图片资源
└── README.md               # 项目说明
```

## 🛠️ 开发指南

### 添加新角色
使用开发者模式可以轻松添加新的奥特曼或怪兽：
1. 点击右上角"开发者模式"
2. 输入密码进入管理界面
3. 选择相应标签页，点击"添加"按钮
4. 填写角色信息并上传图片
5. 保存即可

### 数据结构
详细的数据结构说明请参考 `js/bmob-config.js` 中的模型定义。

### 自定义样式
主要样式文件为 `css/main.css`，使用CSS变量便于主题定制：
```css
:root {
    --primary-color: #0066cc;
    --secondary-color: #ffd700;
    --accent-color: #ff4444;
}
```

## 📱 响应式支持

- **桌面端** (≥1200px): 完整功能展示
- **平板端** (768px-1199px): 优化布局适配
- **手机端** (<768px): 移动优先设计

## 🎯 功能特性

### 搜索与筛选
- 实时搜索建议
- 多条件筛选
- 搜索历史记录
- 结果高亮显示

### 收藏管理
- 本地存储收藏
- 分类收藏展示
- 收藏数据导入/导出
- 收藏统计分析

### 数据对比
- 多角色能力对比
- 雷达图可视化
- 详细参数表格
- 技能对比分析

### 时间轴功能
- 系列历史展示
- 重要事件标记
- 时代筛选功能
- 交互式浏览

## 🚀 部署到GitHub Pages

### 自动部署
1. Fork此项目到您的GitHub账户
2. 在项目设置中启用GitHub Pages
3. 选择主分支作为发布源
4. 配置Bmob安全域名为您的GitHub Pages URL

### 手动部署
1. 将所有文件推送到GitHub仓库的main分支
2. 确保index.html在根目录
3. 在仓库设置中启用Pages功能
4. 访问 `https://your-username.github.io/repository-name`

## 🤝 贡献指南

欢迎提交Issue和Pull Request！

### 贡献方式
1. Fork项目
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启Pull Request

## 📄 许可证

本项目基于MIT许可证开源 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 🙏 致谢

- [Bootstrap](https://getbootstrap.com/) - 前端框架
- [Chart.js](https://www.chartjs.org/) - 图表库
- [Font Awesome](https://fontawesome.com/) - 图标库
- [Bmob](https://www.bmob.cn/) - 后端云服务

## 📞 联系方式

如有问题或建议，请通过以下方式联系：
- 提交 [GitHub Issue](https://github.com/your-username/ultraman-guide/issues)
- 发送邮件到：your-email@example.com

---

⭐ 如果这个项目对您有帮助，请给个Star支持一下！