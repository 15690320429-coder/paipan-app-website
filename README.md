# 九维智慧官网 - 部署说明

## 目录结构

```
website/
├── index.html          # 主页
├── privacy.html        # 隐私政策页面
├── terms.html          # 用户协议页面
├── css/
│   └── style.css       # 主样式文件
├── js/
│   └── main.js         # 交互脚本
└── images/             # 图片资源目录
    ├── logo.png        # 应用Logo (建议尺寸: 200x200px)
    ├── favicon.png     # 网站图标 (建议尺寸: 32x32px)
    ├── app-screenshot-1.png  # Hero区域手机截图 (建议尺寸: 256x512px)
    ├── screenshot-1.png      # 八字排盘截图 (建议尺寸: 240x480px)
    ├── screenshot-2.png      # 紫微斗数截图 (建议尺寸: 240x480px)
    ├── screenshot-3.png      # 六爻占卜截图 (建议尺寸: 240x480px)
    └── screenshot-4.png      # 命理书籍截图 (建议尺寸: 240x480px)
```

## 需要替换的图片

请将以下图片放入 `images/` 目录：

| 文件名 | 用途 | 建议尺寸 |
|--------|------|----------|
| `logo.png` | 应用Logo | 200×200px |
| `favicon.png` | 浏览器图标 | 32×32px |
| `app-screenshot-1.png` | 首屏手机展示 | 256×512px |
| `screenshot-1.png` | 八字排盘截图 | 240×480px |
| `screenshot-2.png` | 紫微斗数截图 | 240×480px |
| `screenshot-3.png` | 六爻占卜截图 | 240×480px |
| `screenshot-4.png` | 命理书籍截图 | 240×480px |

> **注意**: "更多功能"展示区域已改为文字说明卡片，无需提供截图。

### 图片要求

1. **格式**: 推荐使用 PNG 格式（支持透明背景）
2. **质量**: 确保图片清晰，但文件大小适中（建议单张 < 500KB）
3. **比例**: 手机截图保持 9:16 或类似的竖屏比例
4. **背景**: Logo 建议使用透明背景

## 部署到 GitHub Pages

### 方法一：直接上传

1. 登录 GitHub，进入你的仓库 `paipan-app-website`
2. 删除原有文件（或创建新分支）
3. 上传 `website/` 目录下的所有文件到仓库根目录
4. 确保 `index.html` 在仓库根目录
5. 在仓库 Settings → Pages 中启用 GitHub Pages

### 方法二：使用 Git 命令

```bash
# 克隆你的仓库
git clone https://github.com/15690320429-coder/paipan-app-website.git
cd paipan-app-website

# 删除原有文件（保留 .git 目录）
rm -rf *

# 复制新网站文件
cp -r /path/to/website/* .

# 添加图片文件到 images/ 目录

# 提交并推送
git add .
git commit -m "重新设计官网 - 九维智慧"
git push origin main
```

## 自定义修改

### 修改联系邮箱

当前联系邮箱设置为：`15690320429@163.com`

如需修改，在 `index.html` 中搜索并替换该邮箱地址。

### 应用上线后的修改

当应用正式上线后，需要修改以下内容：

1. **即将发布区域**: 改为下载按钮和二维码
2. **Hero按钮**: 将"获取发布通知"改为"立即下载"
3. **页脚状态**: 移除"即将发布"标识

## 网站内容说明

本网站为**即将发布预告版**，满足微信开放平台审核要求：

### ✅ 内容丰富度

| 区块 | 内容 |
|------|------|
| 首屏 Hero | 应用介绍、核心价值、功能预览标签 |
| 功能特性 | 八字排盘、紫微斗数、六爻占卜、更多功能（4个详细卡片） |
| 产品优势 | 算法精准、界面优雅、功能全面、持续更新 |
| 产品截图 | 4张App界面截图 + 1个文字功能卡片轮播展示 |
| 即将发布 | 功能预告、敬请期待 |
| 关于我们 | 团队理念、价值观 |
| 联系方式 | 真实邮箱 |
| 页脚 | 完整导航、隐私政策、用户协议 |

### ✅ 合规性

- 隐私政策页面 (`privacy.html`)
- 用户协议页面 (`terms.html`)
- 真实联系方式
- 无虚假数据

## 技术特性

- **纯静态网站**: 无需后端，GitHub Pages 直接托管
- **响应式设计**: 适配桌面、平板、手机
- **现代 CSS**: CSS 变量、Flexbox、Grid 布局
- **交互动画**: 滚动动画、轮播效果
- **SEO 友好**: 语义化 HTML、Meta 标签

## 浏览器兼容性

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+
- 移动端主流浏览器

---

© 2025 九维智慧
