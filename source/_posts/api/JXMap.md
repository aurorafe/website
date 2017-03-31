---
title: 江西地图
type: api
order: 2
---
  ### new HMap.Map().initMap('target',options)
  - **参数：**
     _ `{String} target` 
     - `{Object} options`
        - `{Object} view` 视图
            
          * `{Array|[x,y]} center` 中心点坐标          
          * `{Array} resolutions` 分辨率           
          * `{Array} fullExtent` 限制范围
          * `{Number} tileSize`
          * `{Array} origin`  切片原点
          * `{Boolean} enableRotation` 是否允许旋转
          * `{String} projection ` 投影坐标系 (EPSG:4326)
          * `{Number} rotation` 倾斜角度
          * `{Number} zoom` 缩放级别
             
      - `{Object} interactions` 交互
           * `{Boolean} mouseWheelZoom` 是否允许滚轮缩放
           * `{Boolean} doubleClickZoom` 是否允许双击放大
           
          > 更多参数详见 openlayer3 API
          
       - `{Array} baseLayers` 图层配置
          * `{String} layerName` 图层名称，用于图层叠加的标识
          * `{Boolean} isDefault` 是否默认显示
          * `{String} layerType` 图层类型
          * `{Boolean} opaque` 图层是否不透明
          * `{Url} layerUrl` 加载图层url地址 
          
 - **用法：**
 
```js
 var cor = [
       {
         "level": 0,
         "resolution": 0.010986328383069278,
         "scale": 4617150
       },
       {
         "level": 1,
         "resolution": 0.005493164191534639,
         "scale": 2308575
       },
       {
         "level": 2,
         "resolution": 0.0027465809060368165,
         "scale": 1154287
       },
       {
         "level": 3,
         "resolution": 0.0013732916427489112,
         "scale": 577144
       },
       {
         "level": 4,
         "resolution": 6.866458213744556E-4,
         "scale": 288572
       },
       {
         "level": 5,
         "resolution": 3.433229106872278E-4,
         "scale": 144286
       },
       {
         "level": 6,
         "resolution": 1.716614553436139E-4,
         "scale": 72143
       },
       {
         "level": 7,
         "resolution": 8.582953794130404E-5,
         "scale": 36071
       },
       {
         "level": 8,
         "resolution": 4.291595870115493E-5,
         "scale": 18036
       },
       {
         "level": 9,
         "resolution": 2.1457979350577466E-5,
         "scale": 9018
       },
       {
         "level": 10,
         "resolution": 1.0728989675288733E-5,
         "scale": 4509
       },
       {
         "level": 11,
         "resolution": 5.363305107141452E-6,
         "scale": 2254
       },
       {
         "level": 12,
         "resolution": 2.681652553570726E-6,
         "scale": 1127
       }
     ];
 var resolutions = [];
 for (var i = 0; i < cor.length; i++) {
   resolutions.push(cor[i].resolution);
 }
 var options = { // 江西地图配置
    view: {
        center: [115.92466595234826, 27.428038204473552], // 地图中心点
        resolutions: resolutions, // 分辨率
        fullExtent: [109.72859368643232, 24.010266905347684, 121.13105988819079, 30.76693489432357],
        tileSize: 256,
        origin: [-400, 399.9999999999998], // 切片原点
        enableRotation: true, // 是否允许旋转
        projection: 'EPSG:4326', // 投影坐标系
        rotation: 0, // 倾斜角度
        zoom: 1, // resolution
        zoomFactor: 2 // 用于约束分变率的缩放因子（高分辨率设备需要注意）
    },
    interactions: {
      altShiftDragRotate: true, // 是否允许`alt + shift`拖拽旋转（默认允许）
      doubleClickZoom: true, // 是否允许双击放大（默认允许）
      mouseWheelZoom: true, // 是否允许滚轮缩放（默认允许）
      shiftDragZoom: true,  // 是否允许`shift`加拖拽缩放（默认允许）
    },
    logo: {},
    baseLayers: [  // 不传时默认加载OSM地图。
      {
        layerName: 'vector',
        isDefault: true,
        layerType: 'TileXYZ',
        opaque: false, //图层是否不透明
        layerUrl: 'http://171.34.40.68:6080/arcgis/rest/services/JXMAP_2016_2/MapServer'
      }
    ]
 }
Maps.initMap('map', options)
```