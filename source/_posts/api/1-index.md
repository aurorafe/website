---
title: 简单地图
type: api
order: 1
---

  ### new HMap.Map().initMap('target',options)
 - **参数：**
   - `{String} target`
   - `{Object} options`
 
 - **用法：**
 
     初始化一个简单地图、必须`new HMap.Map()`
     
     之后必须进行初始化`initMap()`
 
   ``` html
   <div id='map'></div>
   ```
 
   ``` js
   // 创建地图
   var Maps = new HMap.Map()
   //定义options参数
   var options = {
     view: {
         center: [0, 0], // 中心点
         projection: 'EPSG:3857', // 投影坐标系 可不传默认EPSG:3857
         zoom: 4 // resolution
       },
       baseLayers: [] // 不传时默认加载OSM地图。
   }
   // 初始化地图
    Maps.initMap('map',options)
   ```
   
   