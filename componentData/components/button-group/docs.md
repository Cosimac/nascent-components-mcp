按钮组合。
## 何时使用
按钮组合使用时，推荐使用 1 个主操作+n 个次操作，5 个以上操作时。出现更多按钮，默认第一个按钮为主按钮
## API
### ButtonGroup
按钮组配置
| 属性 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| size | 设置按钮大小 | `large` \| `middle` \| `small` | `middle` |  |
| options | 按钮组配置，目前只支持配置 button 组件属性 | Option[] | [] |  |
### Option
| 属性 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| disabled | 按钮失效状态 | boolean | false |  |
| type | 设置按钮类型 | `primary` \| `default` | `default` |  |
| onClick | 点击按钮时的回调 | (event) => void | - |  |
| loading | 设置按钮载入状态 | boolean \| { delay: number } | false |  |
| href | 点击跳转的地址，指定此属性 button 的行为和 a 链接一致 | string | - |  |
| target | 相当于 a 链接的 target 属性，href 存在时生效 | string | - |  |
| title | 按钮文字内容 | string | - |  |
| allowTooltip | 当文本过长时，用于手动控制是否显示省略提示 | boolean | true |  |
| render | 按钮自定义渲染 | `(node: ReactNode) => ReactNode ` | - |  |
