# electron-vue-vite
`Electron` + `Vue3` + `Vite2` integration

## How and Why
- `Vite` is the scaffold of the future

## Command
- npm run dev
- npm run build

## Note
- In the development environment, we need to transform the `Electron` related API into commonjs
- And you can only use ESM
- So far, I've written an `esm2cjs` plugin
  ```ts
  import { ipcRenderer } from 'electron'
  import Store from 'electron-store'
  // Will generate
  const { ipcRenderer } = require("electron")
  const Store = require("electron-store")
  ```
- It works!

- 🚀

- 开发模式下 Electron 相关的 API 需要转换成 commonjs
- 并且你只能用 ESM
- 为此我写了一个 `esm2cjs` 插件

## electron-vue-vite-webpack
- If you are afraid of stepping on the pit, you can consider using this project
[ https://github.com/caoxiemeihao/electron-vue-vite-webpack ]( https://github.com/caoxiemeihao/electron-vue-vite-webpack)
 The production environment is packaged with 'webpack'

- 🚀

- 如果你怕踩坑，可以考虑用这个项目
  [https://github.com/caoxiemeihao/electron-vue-vite-webpack](https://github.com/caoxiemeihao/electron-vue-vite-webpack)
 生产环境使用 `webpack` 打包的

---

![](https://raw.githubusercontent.com/caoxiemeihao/electron-vue-vite/main/screenshot/800x600-2.png)

---

## License

[MIT License](https://opensource.org/licenses/MIT)
