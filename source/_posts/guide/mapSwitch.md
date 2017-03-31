---
title: 底图切换
type: guide
order: 5
---

> 注意事项：
> * 地图必须初始化 `var Maps = new HMap.map('div', {}')`
> * 所有传入的图层必须有 `layerName`（图层名）
> * 初始化图层切换控件 `var layerSwitcher = new HMap.LayerSwitcher(Maps.map)`
> * 传入图层名去控制显示图层 `layerSwitcher.switchLayer(layerName)`