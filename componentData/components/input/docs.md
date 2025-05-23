通过鼠标或键盘输入内容，是最基础的表单域的包装。
## 应用
- 需要用户输入表单域内容时。
- 提供组合型输入框，带搜索的输入框，还可以进行大小选择。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E8%BE%93%E5%85%A5%E6%A1%86)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s12)
## API
### Input
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| addonAfter | 带标签的 input，设置后置标签 | ReactNode | - |  |
| addonBefore | 带标签的 input，设置前置标签 | ReactNode | - |  |
| allowClear | 可以点击清除图标删除内容 | boolean | - |  |
| \*bordered | 是否有边框或者下边框,可选值 true、false、bottom、none | `boolean` \| `string` | true | 4.5.0 |
| defaultValue | 输入框默认内容 | string | - |  |
| disabled | 是否禁用状态，默认为 false | boolean | false |  |
| id | 输入框的 id | string | - |  |
| maxLength | 最大长度 | number | - |  |
| prefix | 带有前缀图标的 input | ReactNode | - |  |
| size | 控件大小。注：标准表单内的输入框大小限制为 `large` | `large` \| `middle` \| `small` | - |  |
| suffix | 带有后缀图标的 input | ReactNode | - |  |
| type | 声明 input 类型，同原生 input 标签的 type 属性，见：[MDN](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/input#属性)(请直接使用 `Input.TextArea` 代替 `type="textarea"`) | string | `text` |  |
| value | 输入框内容 | string | - |  |
| onChange | 输入框内容变化时的回调 | function(e) | - |  |
| onPressEnter | 按下回车的回调 | function(e) | - |  |
| \*\*allowTooltip | 当文本过长时，用于手动控制是否显示省略提示 | boolean | true |  |
| \*\*showCount | 是否展示字数 | boolean \| { formatter: ({ count: number, maxLength?: number }) => string } | false |  |
> 如果 `Input` 在 `Form.Item` 内，并且 `Form.Item` 设置了 `id` 和 `options` 属性，则 `value` `defaultValue` 和 `id` 属性会被自动设置。
Input 的其他属性和 React 自带的 [input](https://reactjs.org/docs/dom-elements.html#all-supported-html-attributes) 一致。
### Input.TextArea
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| allowClear | 可以点击清除图标删除内容 | boolean | false |  |
| autoSize | 自适应内容高度，可设置为 true \| false 或对象：{ minRows: 2, maxRows: 6 } | boolean \| object | false |  |
| bordered | 是否有边框 | boolean | true | 4.5.0 |
| defaultValue | 输入框默认内容 | string | - |  |
| maxLength | 内容最大长度 | number | - | 4.7.0 |
| showCount | 是否展示字数 | boolean \| { formatter: ({ count: number, maxLength?: number }) => string } | false | 4.7.0 (formatter: 4.10.0) |
| value | 输入框内容 | string | - |  |
| onPressEnter | 按下回车的回调 | function(e) | - |  |
| rows | 行数配置：`small`、`middle`、`large`为默认的行数配置 | string \| number | `middle` |  |
| onResize | resize 回调 | function({ width, height }) | - |  |
`Input.TextArea` 的其他属性和浏览器自带的 [textarea](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea) 一致。
#### Input.Group
| 参数 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| compact | 是否用紧凑模式 | boolean | false |
| size | `Input.Group` 中所有的 `Input` 的大小，可选 `large` `default` `small` | string | `default` |
```jsx
<Input.Group>
  <input />
  <input />
</Input.Group>
```
#### Input.Password
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| iconRender | 自定义切换按钮 | (visible) => ReactNode | (visible) => (visible ? &lt;EyeOutlined /> : &lt;EyeInvisibleOutlined />) | 4.3.0 |
| visibilityToggle | 是否显示切换按钮 | boolean | true |  |
#### Input Methods
| 名称 | 说明 | 参数 | 版本 |
| --- | --- | --- | --- |
| blur | 取消焦点 | - |  |
| focus | 获取焦点 | (option?: { preventScroll?: boolean, cursor?: 'start' \| 'end' \| 'all' }) | option - 4.10.0 |
## FAQ
### 为什么我动态改变 `prefix/suffix` 时，Input 会失去焦点？
当 Input 动态添加或者删除 `prefix/suffix` 时，React 会重新创建 DOM 结构而新的 input 是没有焦点的。你可以预设一个空的 `<span />` 来保持 DOM 结构不变：
```jsx
const suffix = condition ? <Icon type="smile" /> : <span />;
<Input suffix={suffix} />;
```
### 为何 TextArea 受控时，`value` 可以超过 `maxLength`？
受控时，组件应该按照受控内容展示。以防止在表单组件内使用时显示值和提交值不同的问题。
