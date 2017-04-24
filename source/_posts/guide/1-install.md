---
title: 安装
type: guide
order: 1
---
### 开发版本

> 重要: Github 仓库的 /dist 文件夹只有在新版本发布时才会更新。如果想要使用 Github 上 HMap 最新的源码，你需要自己构建。

```bash
git clone https://github.com/sakitam-fdd/HMap.git
npm install
npm run dev
npm run build
```

### 更新日志
> v 1.0.0  于2017年3月31日更新
    
### AMD-模块加载器

> 独立下载版本已用 UMD 包装，因此它们可以直接用作 AMD 模块。

    
### ES6方式引入

> vue和angular2搭配es6使用时可以采用

```html
  import HMap from '../dist/HMap'
```
  
```
let Maps = new HMap.Map()
Maps.initMap('map', {})
```



