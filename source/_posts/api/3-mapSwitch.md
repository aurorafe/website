---
title: 底图切换
type: api
order: 3
---

### new HMap.LayerSwitcher(Maps.map)

<p class="tip">要想使用底图切换 需在地图初始化时在baseLayers 添加多个底图或稍后追加多种底图形式</p>
  
 - **参数：**
 
    - `{ol.Map} Maps.map` 地图对象
 
 - **用法：**
```html
  <button onclick="changeLayer('vector')">基本地图</button>
  <button onclick="changeLayer('earth')">影像地图</button>
  <button onclick="changeLayer('panorama')">地形图</button>
  <div id="map"></div>
```

```js
  var layerSwitcher = new HMap.LayerSwitcher(Maps.map);
  
  function changeLayer (type) {
    // type 对应的baseLayers图层组的layerName
    layerSwitcher.switchLayer(type)
  }
```

### 事件
 
  > 切换图层
  ##### `switchLayer(layerName)`
  
  > 返回所有底图的图层名（`Array`）
  ##### `getBaseLayerNames()`
  
  > 设置地图对象
  ##### `setMap(map)`
  
  > 返回地图对象
  ##### `getMap()`
 