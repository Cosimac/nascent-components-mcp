展示一组折叠的下拉菜单。
## 应用
- 多项操作在页面无法展示完全时，采用下拉菜单进行收纳。
- 触发对象多是导航，某个按钮，链接，图标等。
## 相关地址
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s32)
## API
属性
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| disabled | 菜单是否禁用 | boolean | - |  |
| getPopupContainer | 菜单渲染父节点。默认渲染到 body 上，如果你遇到菜单滚动定位问题，试试修改为滚动的区域，并相对其定位。[示例](https://codepen.io/afc163/pen/zEjNOy?editors=0010) | (triggerNode: HTMLElement) => HTMLElement | () => document.body |  |
| overlay | 菜单 | [Menu](/components/menu) \| () => Menu | - |  |
| overlayClassName | 下拉根元素的类名称 | string | - |  |
| overlayStyle | 下拉根元素的样式 | CSSProperties | - |  |
| placement | 菜单弹出位置：`bottomLeft` `bottomCenter` `bottomRight` `topLeft` `topCenter` `topRight` | string | `bottomLeft` |  |
| trigger | 触发下拉的行为, 移动端不支持 hover | Array&lt;`click`\|`hover`\|`contextMenu`> | \[`hover`] |  |
| visible | 菜单是否显示 | boolean | - |  |
| onVisibleChange | 菜单显示状态改变时调用，参数为 `visible` | (visible: boolean) => void | - |  |
`overlay` 菜单使用 [Menu](/components/menu/)，还包括菜单项 `Menu.Item`，分割线 `Menu.Divider`。
> 注意： Menu.Item 必须设置唯一的 key 属性。
### Dropdown.Button
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| buttonsRender | 自定义左右两个按钮 | (buttons: ReactNode\[]) => ReactNode\[] | - |  |
| disabled | 菜单是否禁用 | boolean | - |  |
| icon | 右侧的 icon | ReactNode | - |  |
| overlay | 菜单 | [Menu](/components/menu/) | - |  |
| placement | 菜单弹出位置：`bottomLeft` `bottomCenter` `bottomRight` `topLeft` `topCenter` `topRight` | string | `bottomLeft` |  |
| size | 按钮大小，和 [Button](/components/button/#API) 一致 | string | `default` |  |
| trigger | 触发下拉的行为 | Array&lt;`click`\|`hover`\|`contextMenu`> | \[`hover`] |  |
| type | 按钮类型，和 [Button](/components/button/#API) 一致 | string | `default` |  |
| visible | 菜单是否显示 | boolean | - |  |
| onClick | 点击左侧按钮的回调，和 [Button](/components/button/#API) 一致 | (event) => void | - |  |
| onVisibleChange | 菜单显示状态改变时调用，参数为 `visible` | (visible: boolean) => void | - |  |
### SchemaDropdown.option
| 参数       | 说明                     | 类型                 | 默认值 | 版本 |
| ---------- | ------------------------ | -------------------- | ------ | ---- |
| danger     | 展示错误状态样式         | boolean              | false  |      |
| disabled   | 是否禁用                 | boolean              | false  |      |
| icon       | 菜单图标                 | ReactNode            | -      |      |
| key        | item 的唯一标志          | string               | -      |      |
| title      | 设置收缩时展示的悬浮标题 | string               | -      |      |
| groupTitle | 分组标题                 | string               | -      |      |
| divider    | 分割线                   | boolean              | false  |      |
| children   | 菜单                     | [option](#option)\[] | -      |      |
### SchemaDropDown.Button
支持 Dropdown.Button 相关所有 API 以及[Button](/components/button/)的 API，但是 Button 的 API：icon 不支持进行配置
## FAQ
### 浮层边缘无法完整展示
浮层在屏幕边缘无法完整展示时，会自适应展示方向，但在组件库特殊环境无法体现，此功能在项目中验证通过。
