# Mint UI 定制版

- 风格稍做调整

# Mint UI 官方说明

[![Build Status](https://travis-ci.org/ElemeFE/mint-ui.svg?branch=master)](https://travis-ci.org/ElemeFE/mint-ui)
[![npm](https://img.shields.io/npm/v/mint-ui.svg?maxAge=3600)](https://www.npmjs.com/package/mint-ui)
[![NPM downloads](http://img.shields.io/npm/dm/mint-ui.svg)](https://npmjs.org/package/mint-ui)
![JS gzip size](http://img.badgesize.io/elemefe/mint-ui/master/lib/index.js.svg?compression=gzip&label=gzip%20size:%20JS)
![CSS gzip size](http://img.badgesize.io/elemefe/mint-ui/master/lib/style.css.svg?compression=gzip&label=gzip%20size:%20CSS)
[![Join the chat at https://gitter.im/ElemeFE/mint-ui](https://badges.gitter.im/ElemeFE/mint-ui.svg)](https://gitter.im/ElemeFE/mint-ui?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

> Mobile UI elements for **Vue 2.0**

- [Homepage](http://mint-ui.github.io)
- [Documentation](http://mint-ui.github.io/docs)

<a target='_blank' rel='nofollow' href='https://app.codesponsor.io/link/bD3dKbdDE2F7Ky9LUN1kjTFK/ElemeFE/mint-ui'>
  <img alt='Sponsor' width='888' height='68' src='https://app.codesponsor.io/embed/bD3dKbdDE2F7Ky9LUN1kjTFK/ElemeFE/mint-ui.svg' />
</a>

## Installation
```shell
npm i mint-ui -S

# for Vue 1.x
npm i mint-ui@1 -S
```

## Usage

Import all components.

```javascript
import Vue from 'vue';
import Mint from 'mint-ui';
import 'mint-ui/lib/style.css';

Vue.use(Mint);
```

Or import specified component. (Use [babel-plugin-component](https://www.npmjs.com/package/babel-plugin-component))

```javascript
import { Cell, Checklist } from 'mint-ui';

Vue.component(Cell.name, Cell);
Vue.component(Checklist.name, Checklist);
```


Equals to

```javascript
import Vue from 'vue';
import Mint from 'mint-ui';
import 'mint-ui/lib/style.css';

Vue.use(Mint);

// import specified component

import MtRadio from 'mint-ui/lib/radio';
import 'mint-ui/lib/radio/style.css';

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
    { "libraryName": "mint-ui", "style": true }
  ]]]
}
```

## CDN
RawGit

- https://cdn.rawgit.com/ElemeFE/mint-ui/master/lib/index.js
- https://cdn.rawgit.com/ElemeFE/mint-ui/master/lib/style.css

NPMCDN

- https://unpkg.com/mint-ui/lib/index.js
- https://unpkg.com/mint-ui/lib/style.css

## Development

```shell
npm run dev
```

## Contribution
Please make sure to read the [Contributing Guide](https://github.com/ElemeFE/mint-ui/blob/master/.github/CONTRIBUTING_en-us.md) before making a pull request.

## License
MIT
