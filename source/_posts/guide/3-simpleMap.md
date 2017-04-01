---
title: 简单地图
type: guide
secTitle : basics
order: 3
---

###  引用
  
```html
  <script src='../dist/HMap.min.js'></script>
```

### 创建

```html
  <div id='map'></div>
```

```js
  var Maps = new HMap.Map()
```

### 初始化
```js
  Maps.initMap('map', {})
```

{% raw %}
<div id='map'></div>
<script>
var Maps = new HMap.Map()
var options = {
  view : {
    zoom : 4
  }
}
Maps.initMap('map', options)
</script>
{% endraw %}
