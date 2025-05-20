单选框。
## 何时使用
- 用户需要从一组互斥选择中仅选择一个选项时。
- 和 Select 的区别是，Radio 所有选项默认可见，方便用户在比较中选择，因此选项不宜过多。建议 4 个以内，过多的选项可使用选择器。
- 有时会使用在表格中。
## 文案
选择项应用最简洁，最少的文字描述
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E5%8D%95%E9%80%89)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s10)
## API
### Radio/Radio.Button
| 参数             | 说明                                       | 类型      | 默认值 |
| ---------------- | ------------------------------------------ | --------- | ------ | --- |
| autoFocus        | 自动获取焦点                               | boolean   | false  |
| checked          | 指定当前是否选中                           | boolean   | false  |
| defaultChecked   | 初始是否选中                               | boolean   | false  |
| disabled         | 禁用 Radio                                 | boolean   | false  |
| value            | 根据 value 进行比较，判断是否选中          | any       | -      |
| \*\*icon         | 纯图标单选框，仅用于 Radio.Button          | ReactNode | -      |
| \*\*allowTooltip | 当文本过长时，用于手动控制是否显示省略提示 | boolean   | true   |     |
### RadioGroup
单选框组合，用于包裹一组 `Radio`。
| 参数 | 说明 | 类型 | 默认值 | 版本 |  |
| --- | --- | --- | --- | --- | --- |
| buttonStyle | RadioButton 的风格样式，目前有描边和填色两种风格 | `outline` \| `solid` | `outline` |  |  |
| \*\*border | Radio 的风格样式，是否存在边框 | boolean | `false` |  |  |
| defaultValue | 默认选中的值 | any | - |  |  |
| disabled | 禁选所有子单选器 | boolean | false |  |  |
| name | RadioGroup 下所有 `input[type="radio"]` 的 `name` 属性 | string | - |  |  |
| options | 以配置形式设置子元素 | string\[] \| Array&lt;{ label: string value: string disabled?: boolean }> | - |  |  |
| optionType | 用于设置 Radio `options` 类型 | `default` \| `button` | `default` | 4.4.0 |  |
| size | 大小，只对按钮样式生效 | `large` \| `middle` \| `small` | - |  |  |
| value | 用于设置当前选中的值 | any | - |  |  |
| onChange | 选项变化时的回调函数 | function(e:Event) | - |  |  |
| \*\*direction | 单选框组合排列方式,可选值有`horizontal` `vertical` | string | `horizontal` |  |  |
| \*\*clickArea | 单选框组合垂直排列时单选框点击范围,可选值有`text` `all` | string | `text` |  |  |
## 方法
### Radio
| 名称    | 描述     |
| ------- | -------- |
| blur()  | 移除焦点 |
| focus() | 获取焦点 |
