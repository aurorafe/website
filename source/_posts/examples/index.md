---
title: 简单地图
type: examples
order: 1
---

### 简单地图
  
  
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