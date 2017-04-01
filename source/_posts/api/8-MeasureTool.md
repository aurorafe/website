---
title: 测量
type: api
order: 8
---

### 测量
  
### new HMap.MeasureTool(Maps.map)

<p class="tip">要想使用测量，必须先定义此类</p>

- **参数：**
  
     - `{ol.Map} Maps.map` 地图对象   
     
### 测距

##### `.setUp({ measureType: 'measureLength'})`

- **参数：**
  
     - `{Object} options` 相关参数
          * `{String} measureType` 测量类型 （`measureLength`为测距）
          
- **用法：**
```html
<button onclick="measureTool('measureLength')">测距</button>
```
```js
function measureTool (type) {
  var measure =  new HMap.MeasureTool(Maps.getMap())
  measure.setUp({
    measureType: type
  })
}
```

### 测面

##### `.setUp({ measureType: 'measureArea'})`

- **参数：**
  
     - `{Object} options` 相关参数
          * `{String} measureType` 测量类型 （`measureArea`为测距）
          
- **用法：**
```html
<button onclick="measureTool('measureArea')">测面</button>
```
```js
function measureTool (type) {
  var measure =  new HMap.MeasureTool(Maps.getMap())
  measure.setUp({
    measureType: type
  })
}
```