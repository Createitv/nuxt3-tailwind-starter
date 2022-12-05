# Nuxt3 Tailwind Starter

你是否受够了每次前端开发`npm install [..args]`,重复配置各种前端基本组件库、Lint库、重复部署上线。在N
次以后配置一下午做了一个有好的`Nuxt3`开发Template。

## 项目预览

[演示地址](https://nuxt3-tailwind-start.vercel.app/) [直接修改](https://stackblitz.com/github/Createitv/nuxt3-tailwind-starter/tree/main)

## 功能支持

- [Nuxt 3](https://v3.nuxtjs.org/)
- [Nuxt Content v2](https://content.nuxtjs.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Nuxt Icon](https://nuxt.com/modules/icon)
- [Pinia](https://pinia.vuejs.org/)
- [vee-validate](https://vee-validate.logaretm.com/v4/)
- `useAuthStore` 登录验证
- [@nuxtjs/i18n](https://v8.i18n.nuxtjs.org/)

### 其他

- 🎨 使用Tailwind作为CSS组件库
- 📦 内置多种通用组件和布局
- 💪 Eslint和Stylelint代码检验；
- 🐶 创建Git commit message cn规范校验；
- 🎉 天然支持Vue3、Typescript、Vite等；
- 🍍 集成Pinia作为状态管理；
- 🥤 集成vueuse作为Hooks库；
- 🎊文件式路由、componentsAPI自动导入、组件自动导入等；
- 🎁 集成Nuxt Content作为Markdown文件管理；
- 🎁 集成Nuxt Icon作为SVG图标管理；
- 🎁 集成Nuxt I18n作为国际化管理；
- 🎁 集成Vee-Validate作为表单验证；
- 🎁 集成Vercel作为自动部署；
- 🎁 集成Pnpm作为包管理工具；
- 🎁 集成Github Action作为CI/CD；
- 🎁 集成Prettier作为代码格式化工具；
- 🎁 集成Commitlint作为Git commit message规范校验；
- 🎁 集成Changelog作为自动生成CHANGELOG.md；
- 🎁 集成Husky作为Git commit message规范校验；
- 🎁 集成Lint-staged作为Git commit message规范校验；
- 🎁 集成Prettier作为Git commit message规范校验；
- 🎁 集成Nuxt PWA作为PWA支持；
- 🎁 集成Nuxt Composition API作为Vue3 Composition API支持；
- 🎁 集成Nuxt Image作为图片优化支持；
- 🎁 集成Nuxt Webfont loader作为字体加载支持；
- 🎁 集成Nuxt Style Resources作为全局样式支持；
- 🎁 集成Nuxt Google Analytics作为Google Analytics支持；
- 🎁 集成Nuxt Google Tag Manager作为Google Tag Manager支持；
- 🎁 集成Nuxt Sentry作为Sentry支持；
- 🎁 集成Nuxt Sitemap作为Sitemap支持；
- 🎁 集成Nuxt Robots作为Robots支持；

### 项目预览

![项目预览](https://typora-1300715298.cos.ap-shanghai.myqcloud.com/blogimage-20221201165820159.png)

### 如何使用

```bash
# 克隆项目
git clone https://github.com/Createitv/nuxt3-tailwind-starter
# 进入项目目录
cd nuxt3-tailwind-starter
# 安装依赖
pnpm install
# 启动服务
pnpm dev
```

### 如何部署

```bash
# 构建
pnpm build
# 启动服务
pnpm start
```

### 如何查看

```bash
# 启动服务
pnpm dev
# 打开浏览器
http://localhost:3000
```

### 如何提交

```bash
# 提交代码
git add .
git commit -m 'feat: xxx'
git push
```

### 如何发布

```bash
# 发布代码
git tag v1.0.0
git push origin v1.0.0
```

### Gihub Action自动部署

```yml
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      #  your build commands
      # - run: |
      #    ng build --prod
      - uses: amondnet/vercel-action@v20 # deploy
        with:
          vercel-token: ${{ secrets.VERCEL_TOKEN }} # Required
          github-token: ${{ secrets.GITHUB_TOKEN }} # Optional
          vercel-args: --prod # Optional
          vercel-org-id: ${{ secrets.ORG_ID}} # Required
          vercel-project-id: ${{ secrets.PROJECT_ID}} # Required
          working-directory: .
```

上传Vecel生成的`VERCEL_TOKEN` `ORG_ID ` `PROJECT_ID`到项目的` Action secrets`每次推送`Main`分支自动同步部署到网站上
