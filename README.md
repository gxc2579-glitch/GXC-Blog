# GuXingChen Blog

[![Deploy to GitHub Pages](https://github.com/gxc2579-glitch/GXC-Blog/actions/workflows/deploy.yml/badge.svg)](https://github.com/gxc2579-glitch/GXC-Blog/actions/workflows/deploy.yml)

> Tech Otakus · 记录技术、ACGN 与生活

![GuXingChen Blog](./public/assets/images/hello-gxc-cover.jpg)

GuXingChen Blog 的个人站点源码，使用 **Astro** 构建，**Svelte** 提供交互，**Tailwind CSS** 负责样式。

## 在线预览

https://gxc2579-glitch.github.io/GXC-Blog/

## 特性

- 静态生成，快速加载，SEO 友好
- 亮色 / 暗色模式，响应式布局
- Pagefind 全文搜索
- Markdown / MDX 文章，支持代码块、Mermaid、PlantUML、KaTeX、提醒框、Wiki Link、文章加密等
- 首页随机壁纸，桌面端与移动端使用不同图库
- 音乐播放器、RSS / Atom、文章系列、置顶
- 构建期图片优化与 LQIP 占位

## 本地开发

环境要求：Node.js >= 22、pnpm 11。

```bash
pnpm install
pnpm dev
```

开发服务器默认运行在 `http://localhost:4321`。

## 构建

```bash
pnpm build
pnpm preview
```

构建产物输出到 `dist/`。GitHub Pages 部署由 `.github/workflows/deploy.yml` 自动完成：构建时设置 `GITHUB_PAGES=true`，站点会自动使用 `/GXC-Blog` 子路径。

## 常用命令

| 命令 | 作用 |
|---|---|
| `pnpm dev` | 启动开发服务器 |
| `pnpm build` | 生产构建 |
| `pnpm preview` | 预览构建结果 |
| `pnpm check` | Astro 类型与错误检查 |
| `pnpm type-check` | TypeScript 类型检查 |
| `pnpm lint` / `pnpm format` | Biome 检查 / 格式化 |
| `pnpm new-post <filename>` | 新建文章 |
| `pnpm lqips` | 重新生成图片 LQIP |

## 目录结构

```text
src/
├── components/   # Astro / Svelte 组件
├── config/       # 站点配置
├── content/      # 文章、动态、项目与特殊页
├── layouts/      # 页面布局
├── pages/        # 路由
├── plugins/      # Markdown / 图表 / 图片等构建插件
├── styles/       # 全局样式
└── utils/        # 工具函数
```

站点配置集中在 `src/config/`，文章放在 `src/content/posts/`，首页壁纸位于 `src/assets/images/DesktopWallpaper/` 与 `MobileWallpaper/`。

## 许可

MIT License，详见 [LICENSE](./LICENSE)。
