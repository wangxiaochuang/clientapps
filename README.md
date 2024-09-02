# dioxus

先要安装工具`dioxus`
```sh
cargo install dioxus-cli
```

```sh
cargo generate wangxiaochuang/rustwstpl
> clientapps
cd clientapps
dx new hackernews
# 创建过程如果使用了tailwindcss，可以监控 css 的样式变化
# 它会根据项目里用到的 css，自动生成
cd hackernews
npx tailwindcss -i ./input.css -o ./assets/tailwind.css --watch
# 运行项目
dx serve --hot-reload
```

关于 tailwind，它是一个 css 框架，可以快速开发页面，但是他没有提供组件库，而 flowbit 是基于它的一个组件库

添加`tailwindcss-typography`ui框架

```sh
npm init
yarn add @tailwindcss/typography
yarn add @tailwindcss/forms
```
修改`tailwind.config.js`
```js
module.exports = {
  theme: {
    // ...
  },
  plugins: [
    require('@tailwindcss/typography'),
    require('@tailwindcss/forms')
    // ...
  ],
}
```
