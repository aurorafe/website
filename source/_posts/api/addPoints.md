---
title: 添加点
type: api
order: 4
---

### 添加单点
  ##### addPoint(point,options)
     
 - **参数：**
  
     - `{Object} point` 标准空间要素
        * `{Object} attributes` 属性信息，用于气泡展示等其他要素
          * `{String} id || ID` id必传
          
        * `{ol.geom.Geometry}` 空间位置信息
        
        * `{String}` 要素类型
        
     - `{Object} options` 相关参数
        * `{String} layerName` 图层name
        
 - **用法：**
```html
  <button onclick="addPoint()">添加点</button>
  <div id="addPoint"></div>
```
```js
var point = {
  attributes: {
     ID: '01',
     QLDM: 'Y236360922L0050',
     QLMC: '柏木桥',
     LXBM: 'Y236360922',
     LXMC: '赤兴至排江',
     QLZXZH: '7.4650000000',
     PYZH: '0.0000000000',
     QLQC: '23.0000000000',
     QMQK: '3.5000000000',
     ASYNXFLDM: '1.0000000000',
     XZQHBM: '360922'
    },
    geometry: 'POINT (115.92466595234826 27.428038204473552)',
    geometryType: 'Point'
}
function addPoint () {
  Maps.addPoint(point, {
    layerName: 'test'
  });
}
```

### 添加多点
  ##### addPoints(points,options)
     
 - **参数：**
  
     - `{Array} points` 标准空间要素数组
     - `{Object} options` 相关参数
        
 - **用法：**



