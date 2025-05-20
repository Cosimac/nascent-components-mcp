下拉选择器。选择器支持单选、多选、搜索，以及键盘快捷操作。
## 应用
- 用户选择操作时
- 当选项少时（少于 5 项），建议直接将选项平铺，使用 Radio 是更好的选择
- 使用多选模式时，选项数据量尽量控制在百条的场景，避免卡顿
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E4%B8%8B%E6%8B%89%E9%80%89%E6%8B%A9%E5%99%A8)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#p21)
## 相关组件
- [筛选区选择器](/components/search-select)
## API
### Select props
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| allowClear | 支持清除 | boolean | true |  |
| showSearch | 是否展示搜索框 | boolean | 单选`false` 复选`true` |  |
| fixedSelectLine | 只在多选模式下有效，用于控制选择框的行数，当行数过多时出现滚动条 true\|false，固定一行\|最高 4.5 行 | boolean | `false` |  |
| bordered | 是否有边框 | boolean | true |  |
| clearIcon | 自定义清空图标 | ReactNode | - |  |
| defaultOpen | 是否默认展开下拉菜单 | boolean | - |  |
| defaultValue | 指定默认选中的条目 | string \| string\[]<br />number \| number\[] | - |  |
| disabled | 是否禁用 | boolean | false |  |
| dropdownClassName | 下拉菜单的 className 属性 | string | - |  |
| dropdownMatchSelectWidth | 下拉菜单和选择器同宽。默认将设置 `min-width`，当值小于选择框宽度时会被忽略。false 时会关闭虚拟滚动 | boolean \| number | true |  |
| filterOption | 是否根据输入项进行筛选。当其为一个函数时，会接收 `inputValue` `option` 两个参数，当 `option` 符合筛选条件时，应返回 true，反之则返回 false | boolean \| function(inputValue, option) | true |  |
| getPopupContainer | 菜单渲染父节点。默认渲染到 body 上，如果你遇到菜单滚动定位问题，试试修改为滚动的区域，并相对其定位。[示例](https://codesandbox.io/s/4j168r7jw0) | function(triggerNode) | () => document.body |  |
| maxTagCount | 最多显示多少个 tag，响应式模式会对性能产生损耗 | number \| `responsive` | - | responsive: 4.10 |
| maxTagPlaceholder | 隐藏 tag 时显示的内容 | ReactNode \| function(omittedValues) | - |  |
| maxOptionShow | 下拉面板最多显示多少个下拉选项 | number | 8.5 | 3.5.38 |
| mode | 设置 Select 的模式为单选或多选 | `multiple` \| `single` | `single` |  |
| notFoundContent | 当下拉列表为空时显示的内容 | ReactNode | `Not Found` |  |
| open | 是否展开下拉菜单 | boolean | - |  |
| options | 下拉菜单配置 | `Option[]` | - |  |
| optionRender | 选项自定义结构 | `(option: Option, searchVal: String) => ReactNode` | - |  |
| placeholder | 选择框默认文本 | string | - |  |
| searchPlaceholder | 搜索框默认文本 | string | - |  |
| showArrow | 是否显示下拉小箭头 | boolean | true |  |
| size | 选择框大小 | `large` \| `middle` \| `small` | `middle` |  |
| trigger | 触发下拉行为,仅无边框单选有效 | `hover` \| `click` | `hover` |  |
| suffixIcon | 自定义的选择框后缀图标 | ReactNode | - |  |
| value | 指定当前选中的条目 | string \| string\[]<br />number \| number\[]<br />LabeledValue \| LabeledValue\[] | - |  |
| itemHeight | 选项高度，选项高度与默认值不相等时需传入，需与`optionRender`共同使用才可生效 | number | 32 |  |
| showSearchTag | 多选内容超出展示区域时出现气泡搜索组（仅多选生效） | boolean | true | 3.5.36 |
| onBlur | 失去焦点时回调 | function | - |  |
| onChange | 选中 option，或 input 的 value 变化时，调用此函数 | function(value \| value[], option:Option \| Array&lt;Option>) | - |  |
| onClear | 清除内容时回调 | function | - | 4.6.0 |
| onDeselect | 取消选中时调用，仅在 `multiple` 模式下生效 | function(value[],Array&lt;Option>) | - |  |
| onDropdownVisibleChange | 展开下拉菜单的回调 | function(open) | - |  |
| onFocus | 获得焦点时回调 | function | - |  |
| onInputKeyDown | 按键按下时回调 | function | - |  |
| onMouseEnter | 鼠标移入时回调 | function | - |  |
| onMouseLeave | 鼠标移出时回调 | function | - |  |
| onPopupScroll | 下拉列表滚动时的回调 | function | - |  |
| onSelect | 被选中时调用，参数为选中项的 value | function(value \| value[], option: Option \| Array&lt;Option)) | - |  |
> 注意，如果发现下拉菜单跟随页面滚动，或者需要在其他弹层中触发 Select，请尝试使用 `getPopupContainer={triggerNode => triggerNode.parentElement}` 将下拉弹层渲染节点固定在触发器的父元素中。
### Select Methods
| 名称    | 说明     | 版本 |
| ------- | -------- | ---- |
| blur()  | 取消焦点 |      |
| focus() | 获取焦点 |      |
### Option
| 参数      | 说明        | 类型                    | 默认值 | 版本 |
| --------- | ----------- | ----------------------- | ------ | ---- |
| className | Option 类名 | string                  | -      |      |
| disabled  | 是否禁用    | boolean                 | false  |      |
| label     | 属性文本    | `ReactNode` \| `string` | -      |      |
| value     | 属性值      | string \| number        | -      |      |
| children  | 分组子项    | Option[]                | -      |      |
## FAQ
### 自定义 Option 样式导致滚动异常怎么办？
这是由于虚拟滚动默认选项高度为 `32px`，如果你的选项高度小于该值则需要通过 `listItemHeight` 属性调整，而 `listHeight` 用于设置滚动容器高度：
```tsx
<Select listItemHeight={10} listHeight={250} />
```
注意：`listItemHeight` 和 `listHeight` 为内部属性，如无必要，请勿修改该值。
### 为何无障碍测试会报缺失 `aria-` 属性？
Select 无障碍辅助元素仅在弹窗展开时创建，因而当你在进行无障碍检测时请先打开下拉后再进行测试。对于 `aria-label` 与 `aria-labelledby` 属性缺失警告，请自行为 Select 组件添加相应无障碍属性。
