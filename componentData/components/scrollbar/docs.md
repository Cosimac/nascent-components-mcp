自定义滚动条组件。
## 应用
内容溢出时，可以用过该组件进行查看。
## 相关地址
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s42)
## API
| 成员 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| onScroll | 滚动时的回调事件 | (e) => void |  |  |
| onScrollFrame | Runs inside the animation frame | (values: [Values](#Values)) => void | - |  |
| onScrollStart | 滚动开始时的回调事件 | () => void |  |  |
| onScrollStop | 滚动停止时的回调事件 | () => void |  |  |
| onUpdate | 在更新组件时调用 | (values: [Values](#Values)) => void |  |  |
| renderView | The element your content will be rendered in | ({ className, style }) => React.ReactNode |  |  |
| renderTrackHorizontal | Horizontal track element | { style }) => React.ReactNode |  |  |
| renderTrackVertical | Vertical track element | { style }) => React.ReactNode |  |  |
| renderThumbHorizontal | Horizontal thumb element | { style }) => React.ReactNode |  |  |
| renderThumbVertical | Vertical thumb element | { style }) => React.ReactNode |  |  |
| hideTracksWhenNotNeeded | 当内容不溢出容器时隐藏轨道(可见性:隐藏) | boolean | false |  |
| thumbSize | Set a fixed size for thumbs in px | number |  |  |
| thumbMinSize | Minimal thumb size in px | number |  |  |
| autoHide | 启用自动隐藏模式 | boolean | true |  |
| autoHideTimeout | 隐藏延迟(毫秒) | number |  |  |
| autoHideDuration | 隐藏动画的持续时间(毫秒） | number | 200 |  |
| autoHeight | 启用自动高度模式 | Boolean | false |  |
| autoHeightMin | 设置自动高度模式的最小高度 | number | 0 |  |
| autoHeightMax | 设置自动高度模式的最大高度 | number | 200 |  |
| universal | 隐藏动画的持续时间(毫秒） | number |  |  |
### Values
| 成员         | 说明               | 类型   | 默认值 | 版本 |
| ------------ | ------------------ | ------ | ------ | ---- |
| top          | 顶部滚动的距离     | number |        |      |
| left         | 横向滚动的距离     | number |        |      |
| clientWidth  | 宽度               | number |        |      |
| clientHeight | 高度               | number |        |      |
| scrollWidth  | 滚动的宽度         | number |        |      |
| scrollHeight | 滚动的高度         | number |        |      |
| scrollLeft   | 滚动距离左侧的距离 | number |        |      |
| scrollTop    | 滚动距离顶部的距离 | number |        |      |
