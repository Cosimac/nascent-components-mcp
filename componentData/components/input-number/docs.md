通过鼠标或键盘，输入范围内的数值。
## 应用
- 当需要获取标准数值时。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E6%95%B0%E5%AD%97%E8%BE%93%E5%85%A5%E6%A1%86)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s33)
## API
### InputNumber
| 成员 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| autoFocus | 自动获取焦点 | boolean | false | - |
| bordered | 是否有边框 | boolean | true | 4.12.0 |
| decimalSeparator | 小数点 | string | - | - |
| defaultValue | 初始值 | number | - | - |
| disabled | 禁用 | boolean | false | - |
| formatter | 指定输入框展示值的格式 | function(value: number \| string): string | - | - |
| keyboard | 是否启用键盘快捷行为 | boolean | true | 4.12.0 |
| max | 最大值 | number | [Number.MAX_SAFE_INTEGER](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Number/MAX_SAFE_INTEGER) | - |
| min | 最小值 | number | [Number.MIN_SAFE_INTEGER](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Number/MIN_SAFE_INTEGER) | - |
| parser | 指定从 `formatter` 里转换回数字的方式，和 `formatter` 搭配使用 | function(string): number | - | - |
| precision | 数值精度，配置 `formatter` 时会以 `formatter` 为准 | number | - | - |
| readOnly | 只读 | boolean | false | - |
| size | 输入框大小 | `large` \| `middle` \| `small` | - | - |
| step | 每次改变步数，可以为小数 | number \| string | 1 | - |
| stringMode | 字符值模式，开启后支持高精度小数。同时 `onChange` 将返回 string 类型 | boolean | false | 4.13.0 |
| value | 当前值 | number | - | - |
| onChange | 变化回调 | function(value: number \| string \| null) | - | - |
| onBlur | 失去焦点的回调 | function(e) | - | - |
| onPressEnter | 按下回车的回调 | function(e) | - | - |
| onStep | 点击上下箭头的回调 | (value: number, info: { offset: number, type: 'up' \| 'down' }) => void | - | 4.7.0 |
| \*\*allowTooltip | 当内容过长时，用于手动控制是否显示省略提示 | boolean | true |  |
| \*\*allowClear | 展示清空按钮 | boolean | false |  |
| \*\*allowValue | 返回输入的值是用户允许输入的（注： 如使用 step 的属性，必须使用该属性） | (value) => boolean | - |  |
| \*\*prefix | 带有前缀图标的 input | ReactNode | - |  |
| \*\*suffix | 带有后缀图标的 input | ReactNode | - |  |
### InputNumberGroup
| 成员 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| width | 长度控制 | string ｜ number，css 的 width 属性 | - | 3.5.29 |
| defaultValue | 初始值 | number\[] | - | - |
| disabled | 禁用 | boolean ｜ boolean\[] | false | - |
| value | 当前值 | number\[] \| string\[] | - | - |
| placeholder | 默认值 | string ｜ string\[] | - | - |
| onChange | 变化回调 | function(value: (number \| string \| null)\[] \| undefined \| null | - | - |
| onBlur | 失去焦点回调 | function(value: (number \| string \| null)\[] \| undefined \| null | - | 3.5.37 |
| onStep | 点击上下箭头的回调 | (value: number\[], info: { offset: number, key: number, type: 'up' \| 'down' }) => void | - | 4.7.0 |
更多属性请参考 [InputNumber](#InputNumber)。
## 方法
### InputNumber
| 名称    | 描述     |
| ------- | -------- |
| blur()  | 移除焦点 |
| focus() | 获取焦点 |
## FAQ
### 为何受控模式下，`value` 可以超出 `min` 和 `max` 范围？
在受控模式下，开发者可能自行存储相关数据。如果组件将数据约束回范围内，会导致展示数据与实际存储数据不一致的情况。这使得一些如表单场景存在潜在的数据问题。
### 为何动态修改 `min` 和 `max` 让 `value` 超出范围不会触发 `onChange` 事件？
`onChange` 事件为用户触发事件，自行触发会导致表单库误以为变更来自用户操作。我们以错误样式展示超出范围的数值。
