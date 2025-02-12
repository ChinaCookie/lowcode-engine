<p align="center">
  <a href="http://lowcode-engine.cn">
    <img width="200" src="https://img.alicdn.com/imgextra/i3/O1CN01i8K9cD1d0HU7TjDtv_!!6000000003673-2-tps-500-591.png">
  </a>
</p>

<h1 align="center">LowCodeEngine</h1>

<div align="center">

An enterprise-class low-code technology stack for scale-out design

[![NPM version][npm-image]][npm-url] [![NPM downloads][download-image]][download-url]

[![Discussions][discussions-image]][discussions-url] [![][issues-helper-image]][issues-helper-url] [![Issues need help][help-wanted-image]][help-wanted-url]

[npm-image]: https://img.shields.io/npm/v/@alilc/lowcode-engine.svg?style=flat-square
[npm-url]: http://npmjs.org/package/@alilc/lowcode-engine

[download-image]: https://img.shields.io/npm/dm/@alilc/lowcode-engine.svg?style=flat-square
[download-url]: https://npmjs.org/package/@alilc/lowcode-engine
[help-wanted-image]: https://flat.badgen.net/github/label-issues/alibaba/lowcode-engine/help%20wanted/open
[help-wanted-url]: https://github.com/alibaba/lowcode-engine/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22
[discussions-image]: https://img.shields.io/badge/discussions-on%20github-blue?style=flat-square
[discussions-url]: https://github.com/alibaba/lowcode-engine/discussions

[issues-helper-image]: https://img.shields.io/badge/using-issues--helper-orange?style=flat-square
[issues-helper-url]: https://github.com/actions-cool/issues-helper

</div>

[![](https://img.alicdn.com/imgextra/i4/O1CN01GhzQuE1rnenyCCQTF_!!6000000005676-0-tps-2878-1588.jpg)](http://lowcode-engine.cn)

English | [简体中文](./README-zh_CN.md)

## ✨ Features

- 🌈 An extension-oriented kernel engine extracted from an enterprise-level low-code platform, pursuing the design concept of the smallest kernel and the strongest ecology
- 📦 Out-of-the-box high-quality ecological elements, including material systems, setters, plugins, etc.
- ⚙️ A complete tool chain, supporting the full-link R&D cycle of ecological elements such as material systems, setters, and plug-ins
- 🔌 Powerful expansion capability, has supported nearly 100 various vertical low-code platforms
- 🛡 Developed with TypeScript, providing complete type definition files

## 🎯 Compatible Environments

- Modern browsers (Chrome >= 80, Edge >= 80, last 2 safari versions, last 2 firefox versions)

## 📚 Engine Protocol

The engine fully implements the "Alibaba Mid-Backend Front-End Basic Construction Protocol Specification" and "Alibaba Mid-Backend Front-End Material Protocol Specification". The protocol stack is a key part of whether materials in the low-code field can be circulated.

![image](https://user-images.githubusercontent.com/1195765/150266126-fef3e3a9-d6a4-4f8e-8592-745f1a344162.png)

## 🌰 Usage example

```bash
npm install @alilc/lowcode-engine --save-dev
```

> **TIPS: Only cdn import is supported, npm package is used to provide code hinting capabilities such as typings**

```ts
import { init, skeleton } from '@alilc/lowcode-engine';

skeleton.add({
  area: 'topArea',
  type: 'Widget',
  name: 'logo',
  content: YourFantaticLogo,
  contentProps: {
    logo:
      'https://img.alicdn.com/tfs/TB1_SocGkT2gK0jSZFkXXcIQFXa-66-66.png',
    href: '/',
  },
  props: {
    align: 'left',
    width: 100,
  },
});

init(document.getElementById('lce'));
```

### Engineering configuration:
```json
{
  "externals": {
    "@alilc/lowcode-engine": "var window.AliLowCodeEngine",
    "@alilc/lowcode-engine-ext": "var window.AliLowCodeEngineExt"
  }
}
```

### cdn optional method:
#### Method 1: alifd cdn
```html
https://alifd.alicdn.com/npm/@alilc/lowcode-engine@1.0.0/dist/js/engine-core.js

https://alifd.alicdn.com/npm/@alilc/lowcode-react-simulator-renderer@1.0.0/dist/js/react-simulator-renderer.js
```

#### Method 2: unpkg
```html
https://unpkg.com/@alilc/lowcode-engine@1.0.0/dist/js/engine-core.js

https://unpkg.com/@alilc/lowcode-react-simulator-renderer@1.0.0/dist/js/react-simulator-renderer.js
```

#### Method 3: jsdelivr
```html
https://cdn.jsdelivr.net/npm/@alilc/lowcode-engine@1.0.0/dist/js/engine-core.js

https://cdn.jsdelivr.net/npm/@alilc/lowcode-react-simulator-renderer@1.0.0/dist/js/react-simulator-renderer.js
```

#### Method 4: Use your own cdn
Pass the files under packages/engine/dist and packages/(react|rax)-simulator-renderer/dist in the source code to your cdn provider

## 🔗 Related Links

- [Official website home page](http://lowcode-engine.cn/)
- [Demo Play Now](http://lowcode-engine.cn/demo) | [Engine Demo Repository](https://github.com/alibaba/lowcode-demo)
- [Official Materials](https://github.com/alibaba/lowcode-materials)
- [official setter](https://github.com/alibaba/lowcode-engine-ext)
- [Official plugin (plugin)](https://github.com/alibaba/lowcode-plugins)
- [Ecological elements (materials, setters, plugins) toolchain](https://www.yuque.com/lce/doc/ulvlkz)
- [User Documentation](http://lowcode-engine.cn/docV2)
- [API](http://lowcode-engine.cn/docV2/vlmeme)

## 💻 Local debugging

```bash
$ git clone git@github.com: alibaba/lowcode-engine.git
$ cd lowcode-engine
$ npm install
$ npm run setup
$ npm start
```

> 📢 npm access speed is slow, Alibaba employees can use tnpm, other students recommend using cnpm or specifying a mirror registry.
>
> 📢 node version limited to 14
>
> 📢 Windows environment must use [WSL](https://docs.microsoft.com/zh-cn/windows/wsl/install), other terminals are not guaranteed to work normally

After lowcode-engine is started, several umd files are provided, which can be debugged in combination with the [lowcode-demo](https://github.com/alibaba/lowcode-demo) project. Refer to the file proxy rules [here](https:/ /www.yuque.com/lce/doc/glz0fx).

## 🤝 Participate in co-construction

Please read first:
1. [How to configure the engine debugging environment? ](https://www.yuque.com/lce/doc/glz0fx)
2. [About the R&D collaboration process of the engine](https://www.yuque.com/lce/doc/contributing)
3. [Engineering Configuration of Engine](https://www.yuque.com/lce/doc/gxwqg6)

> Strongly recommend reading ["The Wisdom of Asking Questions"](https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way), ["How to Ask Questions to the Open Source Community"](https: //github.com/seajs/seajs/issues/545) and [How to Report Bugs Effectively](http://www.chiark.greenend.org.uk/%7Esgtatham/bugs-cn.html), [ "How to Submit Unanswerable Questions to Open Source Projects"](https://zhuanlan.zhihu.com/p/25795393), better questions are easier to get help. (This paragraph refers to [antd](https://github.com/ant-design/ant-design))