滚动加载下拉选择器。
## 何时使用
- 当无法取到全量数据，可使用该组件实现滚动加载。
## API
基于 SelectOrigin 改造，不支持属性：`filterOption`、`labelInValue`、`autoClearSearchValue`、`onPopupScroll`，如需查看其他支持配置 API，请至：[SelectOrigin](/components/select-origin/#API) 查看。
### Select Async props
| 参数         | 说明                       | 类型     | 默认值 | 版本 |
| ------------ | -------------------------- | -------- | ------ | ---- |
| \*\*loadMore | 当用户请求更多项目时的回调 | function | -      |      |
| \*\*hasMore  | 是否有更多的项目要加载     | Boolean  | false  |      |
