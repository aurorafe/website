---
title: 周边搜索
type: api
order: 7
---

### 周边搜索

### new HMap.CustomCircle(Maps.map, options).initCustomCircle()
 - **参数：**
  
     - `{ol.Map} Maps.map` 地图对象        
     - `{Object} options` 相关参数
        * `{Array | [x,y]} center` 中心点
        * `{Number} distance` 半径（范围）
        * `{ol.style.Style} style` 样式
           > 更多详情参数请见openlayer3 API
        * `{Object} centerPoint`
           * `{String} src` 中心点样式（url\base64）
        * `{Function} successCallback` 加载成功返回

 - **用法：**

```html
  <button onclick="customCircle()">开启周边搜索</button> 
```
```js
function customCircle() {
  var coordinate = []
  var options = {
    center: coordinate,
    successCallback: function (geometry, center, radius) {
      // 成功后 通过返回的信息去查询服务 加载周边POI等
    }
  }
  var customCircle = new HMap.CustomCircle(Maps.map, options)
  customCircle.initCustomCircle()
}
```

### 事件

> 返回geometry对象
##### `_getGeometry()`
  return ol.geom.Circle() 

> 返回标准WKT数据
##### `_getWKT()`

> 返回中心点坐标
##### `_getCenter()`
  return Array
  
> 返回圆的半径 
##### `_getRadius()`
  return string  
  
> 返回圆的第一个坐标
##### `_getFirstCoordinate()`
return Array

> 返回圆的最后一个坐标
##### `_getLastCoordinate()`
return Array

> 设置圆的半径
##### `_setRadius(distance)`
 - **参数：**
    * `{Number} distance` 查询范围

> 设置圆的中心点
##### `_setCenter(center)`
 - **参数：**
    * `{Array | [x,y]} center` 中心点

> 设置圆的中心点样式
##### `_setCenterPoint(src)`
 - **参数：**
    * `{String} src` url/base64

> 执行结束事件
##### `successCallback(geometry,center,distance)`
 - **参数：**
   * `{WKT} geometry` 标准WKT数据
   * `{Array} center` 中心点
   * `{Number} distance` 半径（范围）
