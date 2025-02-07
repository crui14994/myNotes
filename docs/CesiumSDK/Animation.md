## Animation

#### 设置视图到某一点 setView

- @param

| 参数名   | type   | 描述 | 默认值 |
| -------- | ------ | ---- | ------ |
| position | Object | 坐标 | -      |

```js
CM.Animation.setView({
  lng: "109.029098",
  lat: "32.690817",
  height: "100000",
  heading: "0", //可不传，默认为0
  pitch: "-90", //可不传，默认为-90
  roll: "0", //可不传，默认为0
});
```

#### 异步设置摄像机以查看提供的一个或多个实体或数据源 zoomTo

用法与 cesium 官方[文档](http://cesium.xin/cesium/cn/Documentation1.62/Viewer.html?classFilter=viewer)一致！

- @param

| 参数名 | type   | 描述                                                                       | 默认值 |
| ------ | ------ | -------------------------------------------------------------------------- | ------ |
| target | Object | 实体，实体阵列，实体集合，数据源，要查看的 Cesium3DTileset，点云或图像层。 | -      |
| offset | Object | 在局部东北向上参考系中，距实体中心的偏移量。                               | -      |

```js
CM.Animation.zoomTo(target, new Cesium.HeadingPitchRange(0, -90, 0));
```

#### 开始自转 startIcrf

```js
CM.Animation.startIcrf();
```

#### 停止自转 stopTcrf

```js
CM.Animation.stopTcrf();
```

#### 定位到某个目标 viewerFlyTo

如果在场景中已经添加了各个要素，需要定位到某个目标，显然 viewer. fyTo()是比较合适的；也就是说目标是要素，viewer. fyTo()比较合适。

把相机飞到 entity, entities, 或者 data source 位置。在这些数据还加载和渲染完成后，才能触发 fyTo。

- @param

| 参数名   | type     | 描述                                            | 默认值       |
| -------- | -------- | ----------------------------------------------- | ------------ |
| target   | Object   | 可以是 entity、entities、tilse 或者 data source | -            |
| option   | Object   | 参考 viewer.flyTo 的参数                        | {duration:3} |
| callback | Function | 定位完成的回调函数                              | -            |

```js
CM.Animation.viewerFlyTo(target, { duration: 1 }, () => {});
```

#### 定位到某个坐标 cameraFlyTo

如果是设置相机位置，Camera.fyTo()比较合适。

- @param

| 参数名   | type     | 描述               | 默认值 |
| -------- | -------- | ------------------ | ------ |
| position | Object   | 坐标               | -      |
| callback | Function | 定位完成的回调函数 | -      |
| duration | Function | 飞行时间           | 3      |

```js
CM.Animation.cameraFlyTo(
  {
    lng: "109.029098",
    lat: "32.690817",
    height: "100000",
    heading: "0", //可不传，默认为0
    pitch: "-90", //可不传，默认为-90
    roll: "0", //可不传，默认为0
  },
  () => {},
  3
);
```

#### 相机绕点旋转 setCameraEotateHeading

- @param

| 参数名   | type   | 描述                                         | 默认值 |
| -------- | ------ | -------------------------------------------- | ------ |
| position | Object | 坐标等信息                                   | -      |
| speed    | Number | 飞行一周所需时间，比如 30s, 那么每秒转动度数 | 30     |

```js
let options = {
  lng: 104.06437182811021,
  lat: 30.62274533905387,
  height: 1000,
};

CM.Animation.setCameraEotateHeading(options);

setTimeout(() => {
  //停止旋转
  viewer.clock.stopTime = viewer.clock.startTime;
}, 5000);
```
