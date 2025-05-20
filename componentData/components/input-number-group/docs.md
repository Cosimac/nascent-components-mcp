数字输入框组合效果。
## 何时使用
组合效果。
## API
属性如下
| 成员 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| width | 长度控制 | string/number，css 的 width 属性 | - | - |
| defaultValue | 初始值 | number\[] | - | - |
| disabled | 禁用 | boolean ｜ boolean\[] | false | - |
| value | 当前值 | number\[] \| string\[] | - | - |
| placeholder | 默认值 | string ｜ string\[] | - | - |
| onChange | 变化回调 | function(value: (number \| string \| null)\[] \| undefined \| null | - | - |
| onStep | 点击上下箭头的回调 | (value: number\[], info: { offset: number, key: number, type: 'up' \| 'down' }) => void | - | 4.7.0 |
更多属性请参考 [InputNumber](/components/input-number/#API)。
