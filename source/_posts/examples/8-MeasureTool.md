---
title: 测量
type: examples
order: 8
---

### 测量
  
{% raw %}
<button onclick="measureTool('length')">测距</button>
<button onclick="measureTool('area')">测面</button>
<div id="map"></div>
<script>
var Maps = new HMap.Map();
Maps.initMap('map', {
  view: {
    center: [0, 0],
    enableRotation: true, // 是否允许旋转
    projection: 'EPSG:3857',
    rotation: 0,
    zoom: 0, // resolution
    zoomFactor: 2 // 用于约束分变率的缩放因子（高分辨率设备需要注意）
  },
  logo: {},
//    baseLayers: [] // 不传时默认加载OSM地图。
});
var measure =  new HMap.MeasureTool(Maps.getMap());
function measureTool (type) {
  if (type == 'length') {
    measure.setUp({
      measureType: 'measureLength'
    });
  } else {
    measure.setUp({
      measureType: 'measureArea'
    });
  }
}
</script>
{% endraw %}