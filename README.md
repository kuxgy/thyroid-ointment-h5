# 甲状腺散结保健膏 - 产品介绍静态网站

## 目录结构

```
甲状腺散结保健膏-静态网站/
├── index.html          # 网站入口（首页）
├── robots.txt          # 搜索引擎爬虫规则
├── README.md           # 本说明文件
└── assets/             # 静态资源目录
    ├── product-box.jpg     # 产品包装图
    └── product-scene.jpg   # 产品实景图
```

## 部署方式

### 方式一：任意静态托管平台（推荐）

将整个目录上传至以下任一平台：

- **Vercel** / **Netlify**：拖拽目录即可部署，自动分配域名
- **GitHub Pages**：推送到仓库后在 Settings 中开启 Pages
- **Gitee Pages**：国内访问速度更快
- **腾讯云 COS** / **阿里云 OSS**：配置静态网站托管
- **七牛云**：对象存储 + 静态网站托管

### 方式二：自有服务器

将目录上传至服务器 Web 根目录（如 Nginx 的 `/usr/share/nginx/html/` 或 Apache 的 `/var/www/html/`），确保 `index.html` 为默认首页。

Nginx 示例配置：

```nginx
server {
    listen 80;
    server_name your-domain.com;
    root /var/www/thyroid-cream;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }

    # 静态资源缓存
    location ~* \.(jpg|jpeg|png|gif|ico|css|js)$ {
        expires 30d;
        add_header Cache-Control "public, immutable";
    }
}
```

### 方式三：本地预览

直接双击 `index.html` 用浏览器打开即可预览。

## 技术说明

- **纯静态页面**：无后端依赖，单文件 HTML + 内联 CSS/JS
- **响应式设计**：移动端优先，适配手机、平板、桌面
- **SEO 优化**：完整 meta 标签、Open Graph、Twitter Card、JSON-LD 结构化数据
- **无障碍**：支持键盘操作、语义化标签、尊重 reduced-motion
- **字体**：使用 Noto Serif SC（标题）+ Noto Sans SC（正文），通过 CDN 加载

## 合规声明

本页面为保健用品介绍页面，所有产品信息均来源于产品包装及官方资料。

- 本品为保健用品，不可代替药品和医疗器械的治疗
- 页面未使用极限词、未承诺疗效、未留联系方式
- 如身体持续不适或症状加重，请及时前往正规医疗机构就诊

## 品牌信息

- 品牌：雲茜姐姐
- 运营主体：雲茜科技有限公司
- 生产达标证号：豫健用生【2022】第0021号
- 产品达标证号：豫健用品【2024】第0774号
- 产品责任险：中国人民保险（PICC）承保
