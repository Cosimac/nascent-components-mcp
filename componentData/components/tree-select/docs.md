树型选择控件。
## 应用
类似 Select 的选择控件，可选择的数据结构是一个树形结构时，可以使用 TreeSelect，例如公司层级、学科系统、分类目录等等。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E6%A0%91%E9%80%89%E6%8B%A9)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s30)
## 相关组件
- [筛选区树选择](/components/search-tree-select)
## API
### Tree props
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- | --- |
| allowClear | 显示清除按钮 | boolean | true |  |
| autoClearSearchValue | 当多选模式下值被选择，自动清空搜索框 | boolean | true |  |
| bordered | 是否显示边框 | boolean | true |  |
| defaultValue | 指定默认选中的条目 | string \| string\[] | - |  |
| disabled | 是否禁用 | boolean | false |  |
| dropdownClassName | 下拉菜单的 className 属性 | string | - |  |
| dropdownMatchSelectWidth | 下拉菜单和选择器同宽。默认将设置 `min-width`，当值小于选择框宽度时会被忽略。false 时会关闭虚拟滚动 | boolean \| number | true |  |
| dropdownStyle | 下拉菜单的样式 | object | - |  |
| fixedSelectLine | 只在多选模式下有效，用于控制选择框的行数，当行数过多时出现滚动条 true\|false，固定一行\| 最高 4.5 行 | boolean | `false` |  |
| getPopupContainer | 菜单渲染父节点。默认渲染到 body 上，如果你遇到菜单滚动定位问题，试试修改为滚动的区域，并相对其定位。[示例](https://codepen.io/afc163/pen/zEjNOy?editors=0010) | function(triggerNode) | () => document.body |  |
| labelInValue | 是否把每个选项的 label 包装到 value 中，会把 value 类型从 `string` 变为 {value: string, label: ReactNode, halfChecked(treeCheckStrictly 时有效): string\[] } 的格式 | boolean | false |  |
| listHeight | 设置弹窗滚动高度 | number | 256 |  |
| loadData | 异步加载数据 | function(node) | - |  |
| maxTagCount | 最多显示多少个 tag，响应式模式会对性能产生损耗 | number \| `responsive` | - | responsive: 4.10 |
| maxTagPlaceholder | 隐藏 tag 时显示的内容 | ReactNode \| function(omittedValues) | - |  |
| multiple | 支持多选（当设置 treeCheckable 时自动变为 true） | boolean | false |  |
| placeholder | 选择框默认文字 | string | - |  |
| searchValue | 搜索框的值，可以通过 `onSearch` 获取用户输入 | string | - |  |
| showArrow | 是否显示 `suffixIcon`，单选模式下默认 `true` | boolean | - |  |
| showSearch | 是否支持搜索框 | boolean | true |  |
| size | 选择框大小 | `large` \| `middle` \  | `small` | - |  |
| suffixIcon | 自定义的选择框后缀图标, 多选模式下必须同时设置 `showArrow` 为 true | ReactNode | - |  |
| switcherIcon | 自定义树节点的展开/折叠图标 | ReactNode | - |  |
| treeCheckStrictly | `checkable` 状态下节点选择完全受控（父子节点选中状态不再关联），会使得 `labelInValue` 强制为 true。 注意 onchange 方法的 value 参数会由数组变成对象{checked,halfChecked},checked 数组可直接设置为组件的 value | boolean | false |  |
| treeData | treeNodes 数据，如果设置则不需要手动构造 TreeNode 节点（value 在整个树范围内唯一） | array&lt;{value, title, children, \[disabled, disableCheckbox, selectable, checkable]}> | \[] |  |
| defaultExpandAll | 默认展开所有树节点 | boolean | true |  |
| defaultExpandedKeys | 默认展开的树节点 | string\[] | - |  |
| expandedKeys | 设置展开的树节点 | string\[] | - |  |
| treeNodeLabelProp | 作为显示的 prop 设置 | string | `title` |  |
| titleRender | 自定义渲染节点 | (nodeData) => ReactNode | - |  |
| value | 指定当前选中的条目 | string \| string\[] | - |  |
| virtual | \[慎用，功能不完善，在部分情况下横向滚动功能缺失\]设置 true 时打开虚拟滚动 | boolean | false | 4.1.0 |
| onChange | 选中树节点时调用此函数 | function(value, label, extra) | - |  |
| onDropdownVisibleChange | 展开下拉菜单的回调 | function(open) | - |  |
| onSearch | 文本框值变化时回调 | function(value: string) | - |  |
| onTreeExpand | 展示节点时调用 | function(expandedKeys) | - |  |
### Tree 方法
| 名称    | 描述     | 版本 |
| ------- | -------- | ---- |
| blur()  | 移除焦点 |      |
| focus() | 获取焦点 |      |
### TreeNode props
> 建议使用 treeData 来代替 TreeNode，免去手工构造麻烦
| 参数            | 说明                                               | 类型      | 默认值 | 版本 |
| --------------- | -------------------------------------------------- | --------- | ------ | ---- |
| checkable       | 当树为 Checkbox 时，设置独立节点是否展示 Checkbox  | boolean   | -      |      |
| disableCheckbox | 禁掉 Checkbox                                      | boolean   | false  |      |
| disabled        | 是否禁用                                           | boolean   | false  |      |
| isLeaf          | 是否是叶子节点                                     | boolean   | false  |      |
| key             | 此项必须设置（其值在整个树范围内唯一）             | string    | -      |      |
| selectable      | 是否可选                                           | boolean   | true   |      |
| title           | 树节点显示的内容                                   | ReactNode | `---`  |      |
| value           | 默认根据此属性值进行筛选（其值在整个树范围内唯一） | string    | -      |      |
## FAQ
### onChange 时如何获得父节点信息？
从性能角度考虑，我们默认不透出父节点信息。你可以这样获得：<https://codesandbox.io/s/wk080nn81k>
### 自定义 Option 样式导致滚动异常怎么办？
请参考 Select 的 [FAQ](/components/select)。
