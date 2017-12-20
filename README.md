# Mint UI 定制版

- 风格稍做调整

[![Build Status](https://travis-ci.org/njfed/mint-ui.svg?branch=wec-mint-ui)](https://travis-ci.org/njfed/mint-ui)
[![npm](https://img.shields.io/npm/v/wec-mint-ui.svg?maxAge=3600)](https://www.npmjs.com/package/wec-mint-ui)

> For Vue 2.x

- [Homepage](https://github.com/njfed/mint-ui)
- [Mint UI 官方文档](http://mint-ui.github.io/docs)

## Installation
```shell
npm i wec-mint-ui -S

## Usage

Import all components.

```javascript
import Vue from 'vue';
import Mint from 'wec-mint-ui';
import 'wec-mint-ui/lib/style.css';

Vue.use(Mint);
```

Or import specified component. (Use [babel-plugin-component](https://www.npmjs.com/package/babel-plugin-component))

```javascript
import { Cell, Checklist } from 'wec-mint-ui';

Vue.component(Cell.name, Cell);
Vue.component(Checklist.name, Checklist);
```


Equals to

```javascript
import Vue from 'vue';
import Mint from 'wec-mint-ui';
import 'wec-mint-ui/lib/style.css';

Vue.use(Mint);

// import specified component

import MtRadio from 'wec-mint-ui/lib/radio';
import 'wec-mint-ui/lib/radio/style.css';

Vue.component(MtRadio.name, MtRadio);
```

## babel-plugin-component
- Auto import css file
- Modular import component

Installation
```shell
npm i babel-plugin-component -D
```

Usage

.babelrc
```json
{
  "plugins": ["other-plugin", ["component", [
    { "libraryName": "wec-mint-ui", "style": true }
  ]]]
}
```

## CDN

- https://unpkg.com/wec-mint-ui/lib/index.js
- https://unpkg.com/wec-mint-ui/lib/style.css

## Development

```shell
npm run dev
```

## Contribution
Just make a pull request.

## License
MIT
