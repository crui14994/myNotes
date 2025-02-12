<!--
 * @Author:
 * @Date: 2023-11-28 14:19:23
 * @LastEditTime: 2025-01-07 13:20:19
 * @LastEditors: caorui 778943319@qq.com
 * @Description:
-->

## Roaming

#### 路径漫游 RoamingStart

- @param

| 参数名       | type   | 描述                       | 默认值   |
| ------------ | ------ | -------------------------- | -------- |
| polylineData | Array  | 路径的 Cartesian3 坐标数组 | -        |
| romingConfig | Object | 巡航配置                   | 参考下表 |

###### romingConfig 属性

| 属性名               | type    | 描述                           | 默认值 |
| -------------------- | ------- | ------------------------------ | ------ |
| modelUrl             | String  | 模型 url 地址                  | -      |
| modelShow            | Boolean | 模型是否显示                   | true   |
| pathShow             | Boolean | 路径是否显示                   | true   |
| polylineShow         | Boolean | 路线是否显示                   | true   |
| interpolationOptions | Object  | 点插值(参考 cesium 点插值配置) | -      |

- @returns

| 返回值        | type   | 描述     | 默认值 |
| ------------- | ------ | -------- | ------ |
| entityRoaming | Object | 巡航对象 | -      |

```js
let entityRoaming = CM.Roaming.RoamingStart(polylineData, {
  modelUrl: "data/model/Cesium_Air.glb",
  interpolationOptions: {
    // interpolationDegree: 5,
    // interpolationAlgorithm: Cesium.LagrangePolynomialApproximation,

    interpolationDegree: 2,
    interpolationAlgorithm: Cesium.HermitePolynomialApproximation,

    // interpolationDegree: 1,
    // interpolationAlgorithm: Cesium.LinearApproximation
  },
});
```

#### 上帝视角开启 openGodView

```js
CM.Roaming.openGodView();
```

#### 跟踪巡航实体 RoamingTrackedEntity

```js
CM.Roaming.RoamingTrackedEntity();
```

#### 停止跟踪巡航实体 StopTrackedEntity

```js
CM.Roaming.StopTrackedEntity();
```

#### 暂停巡航 RoamingPause

```js
CM.Roaming.RoamingPause();
```

#### 继续巡航 RoamingContinue

```js
CM.Roaming.RoamingContinue();
```

#### 改变飞行的速度 RoamingSpeed

- @param

| 参数名 | type   | 描述       | 默认值 |
| ------ | ------ | ---------- | ------ |
| value  | Number | 飞行的速度 | 1      |

```js
CM.Roaming.RoamingSpeed(value);
```

#### 改变飞行倾斜角度 RoamingPitch

- @param

| 参数名 | type   | 描述           | 默认值 |
| ------ | ------ | -------------- | ------ |
| value  | Number | 飞行的倾斜角度 | -40    |

```js
CM.Roaming.RoamingPitch(value);
```

#### 改变飞行高度 RoamingHeight

- @param

| 参数名 | type   | 描述       | 默认值 |
| ------ | ------ | ---------- | ------ |
| value  | Number | 飞行的高度 | 1500   |

```js
CM.Roaming.RoamingHeight(value);
```

#### 改变距中心的距离 RoamingRange

- @param

| 参数名 | type   | 描述         | 默认值 |
| ------ | ------ | ------------ | ------ |
| value  | Number | 距中心的距离 | 50     |

```js
CM.Roaming.RoamingRange(value);
```
