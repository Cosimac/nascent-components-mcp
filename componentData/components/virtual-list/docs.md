## 概述
高效渲染大数据列表和表格的 react 组件。
## API
### VirtualList
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| height | 列表的高度 | Number | - |  |
| width | 列表的宽度 | Number | - |  |
| layout | 布局方向 | String | 'vertical' |  |
| itemCount | 列表中的项目总数 | Number | - |  |
| itemSize | 子级尺寸,`horizontal` 对应 `高度`, `vertical` 对应 `宽度` | Number | - |  |
| overscanCount | 在可见区域之外呈现的项目（行或列）的数量 | Number | 1 |  |
### VirtualList.AutoSizer
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| children | 负责渲染子级的函数 | ({ height: number, width: number }) => PropTypes.element |  |  |
| className | 附加到根 AutoSizer 元素的可选自定义 CSS 类名 | String |  |  |
| defaultHeight | 初始渲染时传递给子级的高度 | Number |  |  |
| defaultWidth | 初始渲染时传递给子级的宽度 | Number |  |  |
| disableHeight | 固定 height | Boolean |  |  |
| disableWidth | 固定 width | Boolean |  |  |
| onResize | 调整大小时调用的回调 | Function |  |  |
| style | 附加到根 AutoSizer 元素的可选自定义内联样式 | Object |  |  |
### VirtualList.InfiniteLoader
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| children | 渲染道具 | ({ onItemsRendered: Function, ref: React$Ref }) => React$Node |  |  |
| isItemLoaded | 负责跟踪每个项目的加载状态的函数。 | (index: number) => boolean |  |  |
| itemCount | 列表中的行数；如果实际数字未知，则可以是任意高数字。 | number |  |  |
| loadMoreItems | 必须加载更多行时调用的回调。它应该返回一个 Promise，一旦所有数据完成加载，该 Promise 就会被解决。 | (startIndex: number, stopIndex: number) => Promise |  |  |
| minimumBatchSize | 一次加载的最小行数；此属性可用于批量请求以减少 HTTP 请求。 | number | 10 |  |
| threshold | 取数据的阈值；默认为 15。阈值为 15 表示当用户在 15 行内滚动时开始加载数据。 | number | 15 |  |
