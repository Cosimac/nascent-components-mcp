用于表格操作列
## 应用
应用于表格的操作列
## API
### Operation
操作组配置
| 属性 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| type | 操作列类型，分为链接操作组、图标操作组、文字图标操作组 | `text` \| `icon` \| `mix` | `text` |  |
| size | 操作列大小尺寸 | `small` \| `middle` \| `large` | `middle` |  |
| maxCount | 操作列最多展示几个按钮,如果超过放入更多操作内 | number | 4 |  |
| options | 表格操作列配置，目前只支持配置部分 button 组件属性 | Option[] | [] |  |
| buttonKey | 每一个按钮 key 的取值，可以是字符串或一个函数 | string \| function(record): string | `key` |  |
### Option
按钮项配置
| 属性 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| danger | 设置危险按钮 | boolean | false |  |
| disabled | 按钮失效状态 | boolean | false |  |
| href | 点击跳转的地址，指定此属性 button 的行为和 a 链接一致 | string | - |  |
| loading | 设置按钮载入状态 | boolean \| { delay: number } | false |  |
| target | 相当于 a 链接的 target 属性，href 存在时生效 | string | - |  |
| onClick | 点击按钮时的回调 | (event) => void | - |  |
| icon | 图标组件 | ReactNode | - |  |
| title | 按钮文字内容 | string | - |  |
| allowTooltip | 当文本过长时，用于手动控制是否显示省略提示 | boolean | true |  |
| render | 按钮自定义渲染 | `(node: ReactNode) => ReactNode ` | - |  |
