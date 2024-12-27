<!--
 * @Author:
 * @Date: 2023-06-30 15:32:17
 * @LastEditTime: 2024-12-27 13:43:36
 * @LastEditors: caorui 778943319@qq.com
 * @Description:
-->

# Material

#### 图片轨迹线材质 PolylineImageTrailMaterial

- @param

| 参数名  | type   | 描述                   | 默认值 |
| ------- | ------ | ---------------------- | ------ |
| options | Object | 材质配置，属性参考下表 | -      |

###### options 属性

| 属性名   | type   | 描述                | 默认值                                   |
| -------- | ------ | ------------------- | ---------------------------------------- |
| image    | String | 图片地址            | -                                        |
| color    | String | 颜色                | Cesium.Color.fromBytes(0, 255, 255, 255) |
| speed    | Number | 速度                | 1                                        |
| repeat   | Object | 重复规则            | { x: 1, y: 1 }                           |
| duration | Number | 动画方向 (1.0/-1.0) | 1.0                                      |

- @returns

| 返回值   | type   | 描述   |
| -------- | ------ | ------ |
| material | Object | 材质。 |

```js
let options = {
  color: new Cesium.Color.fromCssColorString("rgba(255, 134, 27, 1)"),
  speed: 10, // 速度
  image: require("./test.png"),
  repeat: { x: 1, y: 1 },
  direction: 1.0, // 1.0表示正向，-1.0表示反向
};
let material = CM.Material.PolylineImageTrailMaterial(options);
```

#### 颜色流动线材质 PolylineFlowMaterial

- @param

| 参数名  | type   | 描述                   | 默认值 |
| ------- | ------ | ---------------------- | ------ |
| options | Object | 材质配置，属性参考下表 | -      |

###### options 属性

| 属性名   | type   | 描述             | 默认值                                   |
| -------- | ------ | ---------------- | ---------------------------------------- |
| color    | String | 颜色             | Cesium.Color.fromBytes(0, 255, 255, 255) |
| speed    | Number | 速度             | 1                                        |
| percent  | Number | 动画颜色所占比例 | 0.03                                     |
| gradient | Number | 透明程度         | 0.1                                      |

- @returns

| 返回值   | type   | 描述   |
| -------- | ------ | ------ |
| material | Object | 材质。 |

```js
let options = {
  color: new Cesium.Color.fromCssColorString("rgba(255, 134, 27, 1)"),
  speed: 10,
  percent: 0.3, // 比例
  gradient: 0.3, // 透明程度
};
let material = CM.Material.PolylineFlowMaterial(options);
```

#### 发光流动线材质 PolylineLightingTrailMaterial

- @param

| 参数名  | type   | 描述                   | 默认值 |
| ------- | ------ | ---------------------- | ------ |
| options | Object | 材质配置，属性参考下表 | -      |

###### options 属性

| 属性名 | type   | 描述 | 默认值                                   |
| ------ | ------ | ---- | ---------------------------------------- |
| color  | String | 颜色 | Cesium.Color.fromBytes(0, 255, 255, 255) |
| speed  | Number | 速度 | 1                                        |

- @returns

| 返回值   | type   | 描述   |
| -------- | ------ | ------ |
| material | Object | 材质。 |

```js
let options = {
  color: new Cesium.Color.fromCssColorString("rgba(255, 134, 27, 1)"),
  speed: 10,
};
let material = CM.Material.PolylineLightingTrailMaterial(options);
```

#### 轨迹墙体材质 WallTrailMaterial

- @param

| 参数名  | type   | 描述                   | 默认值 |
| ------- | ------ | ---------------------- | ------ |
| options | Object | 材质配置，属性参考下表 | -      |

###### options 属性

| 属性名   | type   | 描述                | 默认值                                   |
| -------- | ------ | ------------------- | ---------------------------------------- |
| color    | Object | 颜色                | Cesium.Color.fromBytes(0, 255, 255, 255) |
| speed    | Number | 速度                | 1                                        |
| duration | Number | 动画方向 (1.0/-1.0) | 1.0                                      |

- @returns

| 返回值   | type   | 描述   |
| -------- | ------ | ------ |
| material | Object | 材质。 |

```js
let options = {
  color: new Cesium.Color.fromCssColorString("rgba(255, 134, 27, 1)"),
  speed: 20,
  direction: -1.0, // 1.0表示从下往上，-1.0表示从上往下
};
let material = CM.Material.WallTrailMaterial(options);
```

#### 线条轨迹墙体材质 WallLineTrailMaterial

- @param

| 参数名  | type   | 描述                   | 默认值 |
| ------- | ------ | ---------------------- | ------ |
| options | Object | 材质配置，属性参考下表 | -      |

###### options 属性

| 属性名   | type   | 描述                | 默认值                                   |
| -------- | ------ | ------------------- | ---------------------------------------- |
| color    | Object | 颜色                | Cesium.Color.fromBytes(0, 255, 255, 255) |
| speed    | Number | 速度                | 1                                        |
| repeat   | Object | 重复规则            | { x: 1, y: 1 }                           |
| duration | Number | 动画方向 (1.0/-1.0) | 1.0                                      |

- @returns

| 返回值   | type   | 描述   |
| -------- | ------ | ------ |
| material | Object | 材质。 |

```js
let options = {
  color: new Cesium.Color.fromCssColorString("rgba(255, 134, 27, 1)"),
  speed: 2,
  repeat: { x: 1, y: 2 },
  direction: -1.0, // 1.0表示从下往上，-1.0表示从上往下
};
let material = CM.Material.WallLineTrailMaterial(options);
```

#### 图片轨迹墙体材质 WallImageTrailMaterial

- @param

| 参数名  | type   | 描述                   | 默认值 |
| ------- | ------ | ---------------------- | ------ |
| options | Object | 材质配置，属性参考下表 | -      |

###### options 属性

| 属性名   | type   | 描述                | 默认值                                   |
| -------- | ------ | ------------------- | ---------------------------------------- |
| image    | String | 图片地址            | -                                        |
| color    | Object | 颜色                | Cesium.Color.fromBytes(0, 255, 255, 255) |
| speed    | Number | 速度                | 1                                        |
| repeat   | Object | 重复规则            | { x: 1, y: 1 }                           |
| duration | Number | 动画方向 (1.0/-1.0) | 1.0                                      |

- @returns

| 返回值   | type   | 描述   |
| -------- | ------ | ------ |
| material | Object | 材质。 |

```js
let options = {
  image: require("../../assets/icon/arrow.png"),
  color: new Cesium.Color.fromCssColorString("rgba(255, 134, 27, 1)"),
  repeat: { x: 100, y: 1 },
  speed: 20,
  direction: 1.0, // 1.0表示正向，-1.0表示反向
};
let material = CM.Material.WallImageTrailMaterial(options);
```

#### 创建水波纹扩散材质 CircleWaveMaterial

- @param

| 参数名  | type   | 描述                   | 默认值 |
| ------- | ------ | ---------------------- | ------ |
| options | Object | 材质配置，属性参考下表 | -      |

###### options 属性

| 属性名   | type   | 描述     | 默认值 |
| -------- | ------ | -------- | ------ |
| color    | String | 颜色     | -      |
| speed    | String | 动画速度 | 3      |
| count    | Number | 波浪数量 | 1      |
| gradient | Number | 渐变曲率 | 0.1    |

- @returns

| 返回值   | type   | 描述   |
| -------- | ------ | ------ |
| material | Object | 材质。 |

```js
let options = {
  color: new Cesium.Color.fromCssColorString("#41A97F"),
  speed: 12.0,
  count: 3,
  gradient: 0.2,
};
let material = CM.Material.CircleWaveMaterial(options);
```
