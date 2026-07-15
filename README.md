# 万相台看板 · UI Demo

这是两个静态 HTML 原型页面,用于万相台投放数据看板的UI方向选型,纯前端(HTML+CSS+JS,图表用 Chart.js CDN),无需构建工具,可直接打开或部署到 GitHub Pages。

## 目录结构

```
.
├── index.html              # 预览入口页,链接到下面两个demo
├── demos/
│   ├── 03_light_enterprise.html   # 浅色企业风
│   └── w1_card_sidebar.html       # 简洁数据卡片 + 侧栏风格
└── .nojekyll               # 告诉GitHub Pages不要用Jekyll处理这些文件
```

## 本地预览

直接双击打开 `index.html`,或者在这个目录下起一个静态服务器:

```
python3 -m http.server 8000
```

然后访问 http://localhost:8000

## 部署到 GitHub Pages

1. 把这个文件夹的内容 push 到你的 GitHub 仓库
2. 仓库 `Settings -> Pages`
3. `Build and deployment` 选择 `Deploy from a branch`,选你 push 的分支和根目录 `/`
4. 保存后等一两分钟,访问 `https://<你的用户名>.github.io/<仓库名>/` 即可看到入口页

## 说明

- 页面里的数据都是前端 mock 出来的演示数据,顶部 `CONFIG.BACKEND_URL`(留空)决定是否尝试连接真实后端接口,真实接入时改这一个字段即可。
- 这两个页面是UI选型阶段的静态demo,不是最终要接入项目的 Vue 组件;选定风格后需要重新用 Vue 实现对应组件,接入实际的历史数据JSON、实时API和AI策略后端。
