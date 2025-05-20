按钮用于开始一个即时操作。标记了一个（或封装一组）操作命令，响应用户点击行为，触发相应的业务逻辑。
## 应用
- 主要按钮：用于主行动点，一个操作区域只能有一个主按钮。
- 次要按钮：1. 没有主次之分的一组行动点；2. 次级按钮。
- 虚线按钮：常用于表单添加操作。
- 链接按钮：1. 用于最次级的行动点； 2. 用于作为外链的行动；点 3. 高重复行动点（表格）。
- 文本按钮：文本次要按钮：不建议单独使用，常常与图标联合使用。
## 文案
按钮上的文本应保持简洁，带着明确、可操作的动词，例如：注册、下一步、下载 ；建议不超过 8 字。
## 相关地址
- 按钮 & 按钮组
  - [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E6%8C%89%E9%92%AE)
  - [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s9)
- 操作组
  - [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s18)
## API
通过设置 Button 的属性来产生不同的按钮样式，推荐顺序为：`type` -> `shape` -> `size` -> `loading` -> `disabled`。
### Button
| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| icon | 设置按钮的图标组件 | ReactNode | - |
| size | 设置按钮大小 | `large` \| `middle` \| `small` | `middle` |
| type | 设置按钮类型 | `primary` \| `default` \| `dashed` \| `link` \| `text` \|`linePrimary` | `default` |
| danger | 设置危险按钮 | boolean | false |
| ghost | 幽灵属性，使按钮背景透明 | boolean | false |
| loading | 设置按钮载入状态 | boolean \| { delay: number } | false |
| disabled | 按钮失效状态 | boolean | false |
| block | 将按钮宽度调整为其父宽度的选项 | boolean | false |
| shape | 设置按钮形状 | `circle` \| `round` | - |
| htmlType | 设置 `button` 原生的 `type` 值，可选值请参考 [HTML 标准](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button#attr-type) | string | `button` |
| href | 点击跳转的地址，指定此属性 button 的行为和 a 链接一致 | string | - |
| target | 相当于 a 链接的 target 属性，href 存在时生效 | string | - |
| onClick | 点击按钮时的回调 | (event) => void | - |
| \*\*allowTooltip | 当文本过长时，用于手动控制是否显示省略提示 | boolean | true |
支持原生 button 的其他所有属性。
### ButtonGroup
| 属性 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| sortMode | 排序方式 | `ascend` \| `default` | `default` |
| size | 设置按钮大小 | `large` \| `middle` \| `small` | `middle` |  |
| options | 按钮组项配置，支持 button 组件所有属性 | [Option](#Option)[] | [] |  |
### Operation
操作组配置
| 属性 | 说明 | 类型 | 可选值 | 默认值 | 版本 |
| --- | --- | --- | --- | --- | --- |
| type | 操作列类型，分为链接操作组、图标操作组、文字图标操作组 | string | `text` \| `icon` \| `mix` | `text` |  |
| size | 操作列大小尺寸 | string | `small` \| `middle` \| `large` | `middle` |  |
| count | 操作列的展示类型值，可以是数字或者字符串类型 | `number` \| `string` | `auto`\|`wrap` | 4 |  |
| options | 操作组项配置，支持 button 组件所有属性 | [Option](#Option)[] | - | [] |  |
| buttonKey | 每一个按钮 key 的取值，可以是字符串或一个函数 | string \| function(record): string | - | `key` |  |
| bordered | 边框 | boolean | - | false |  |
### Operation.calculateWidth
操作组宽度计算参数
| 属性 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| type | 操作列类型，分为链接操作组、图标操作组、文字图标操作组 | `text` \| `icon` \| `mix` | `text` |  |
| size | 操作列大小尺寸 | `small` \| `middle` \| `large` | `middle` |  |
| count | 操作列最多展示几个按钮,如果超过放入更多操作内 | number | 4 |  |
| options | 操作组项配置，支持 button 组件所有属性 | [Option](#Option)[] | [] |  |
### Option
按钮组项配置，除了支持 [Button](#Button) 的所有属性，还支持以下配置
| 属性        | 说明           | 类型                              | 默认值 | 版本 |
| ----------- | -------------- | --------------------------------- | ------ | ---- |
| render      | 按钮自定义渲染 | `(node: ReactNode) => ReactNode ` | -      |      |
| disabledTip | 禁用文字提示   | string                            | -      |      |
## FAQ
### 如何在两个汉字之间自动添加空格？
可以设置 [ConfigProvider](/components/config-provider/#API) 的 `autoInsertSpaceInButton` 为 `true`。
<img src="https://gw.alipayobjects.com/zos/antfincdn/MY%26THAPZrW/38f06cb9-293a-4b42-b183-9f443e79ffea.png" style="box-shadow: none; margin: 0; width: 100px" alt="移除两个汉字之间的空格"  />
## 设计指引
- [我的按钮究竟该放哪儿！？| Ant Design 4.0 系列分享](https://zhuanlan.zhihu.com/p/109644406)
