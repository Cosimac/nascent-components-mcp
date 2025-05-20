警告提示，展现需要关注的信息--用于轮播展示。
## 何时使用
- 多条消息进行轮播
## API
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| options | 警告提示组配置，目前只支持 alter 组件属性 | [Object](/components/alter/#API) | - |  |
### Alert.ErrorBoundary
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| description | 自定义错误内容，如果未指定会展示报错堆栈 | ReactNode | {{ error stack }} |  |
| message | 自定义错误标题，如果未指定会展示原生报错信息 | ReactNode | {{ error }} |  |
