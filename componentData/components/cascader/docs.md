常用于层级较多时的选项选择。
## 应用
- 需要从一组相关联的数据集合进行选择，例如省市区，公司层级，事物分类等。
- 从一个较大的数据集合中进行选择时，用多级分类进行分隔，方便选择。
- 比起 Select 组件，可以在同一个浮层中完成选择，有较好的体验。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E7%BA%A7%E8%81%94%E9%80%89%E6%8B%A9%E5%99%A8)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/%E7%BA%A7%E8%81%94%E9%80%89%E6%8B%A9%E5%99%A8-UI/)
## 相关组件
- 带标题的[筛选区级联选择器](/components/search-cascader)
## API
```jsx
<Cascader options={options} onChange={onChange} />
```
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| allowClear | 是否支持清除 | boolean | true |  |
| autoFocus | 自动获取焦点 | boolean | false |  |
| bordered | 是否有边框 | boolean | true |  |
| clearIcon | 自定义的选择框清空图标 | ReactNode | - |  |
| changeOnSelect | （单选时生效）当此项为 true 时，点选每级菜单选项值都会发生变化，具体见上面的演示 | boolean | false |  |
| className | 自定义类名 | string | - |  |
| defaultValue | 默认的选中项 | string\[] \| number\[] | \[] |  |
| disabled | 禁用 | boolean | false |  |
| displayRender | 选择后展示的渲染函数 | (label, selectedOptions) => ReactNode | label => label.join(`/`) | `multiple`: 4.18.0 |
| dropdownClassName | 自定义浮层类名 | string | - |  |
| dropdownRender | 自定义下拉框内容 | (menus: ReactNode) => ReactNode | - | 4.4.0 |
| expandIcon | 自定义次级菜单展开图标 | ReactNode | - | 4.4.0 |
| expandTrigger | 次级菜单的展开方式，可选 'click' 和 'hover' | string | `click` |  |
| getPopupContainer | 菜单渲染父节点。默认渲染到 body 上，如果你遇到菜单滚动定位问题，试试修改为滚动的区域，并相对其定位。[示例](https://codepen.io/afc163/pen/zEjNOy?editors=0010) | function(triggerNode) | () => document.body |  |
| loadData | 用于动态加载选项，无法与 `showSearch` 一起使用 | (selectedOptions) => void | - |  |
| maxTagCount | 最多显示多少个 tag，响应式模式会对性能产生损耗 | number \| `responsive` | - |  |
| maxTagPlaceholder | 隐藏 tag 时显示的内容 | ReactNode \| function(omittedValues) | - |  |
| notFoundContent | 当下拉列表为空时显示的内容 | string | `Not Found` |  |
| open | 控制浮层显隐 | boolean | - |  |
| options | 可选项数据源 | [Option](#Option)\[] | - |  |
| placeholder | 输入框占位文本 | string | `请选择` |  |
| placement | 浮层预设位置 | `bottomLeft` `bottomRight` `topLeft` `topRight` | `bottomLeft` |  |
| showSearch | 在选择框中显示搜索框 | boolean | true |  |
| size | 输入框大小 | `large` \| `middle` \| `small` | - |  |
| status | 设置校验状态 | 'error' \| 'warning' | - | 4.19.0 |
| style | 自定义样式 | CSSProperties | - |  |
| suffixIcon | 自定义的选择框后缀图标 | ReactNode | - |  |
| tagRender | 自定义 tag 内容，多选时生效 | (props) => ReactNode | - |  |
| value | 指定选中项 | string\[] \| number\[] | - |  |
| onChange | 选择完成后的回调 | (value, selectedOptions) => void | - |  |
| onDropdownVisibleChange | 显示/隐藏浮层的回调 | (value) => void | - |  |
| multiple | 支持多选节点 | boolean | - |  |
| removeIcon | 自定义的多选框清除图标 | ReactNode | - |  |
| dropdownMenuColumnStyle | 下拉菜单列的样式 | CSSProperties | - |  |
| \*checkStrictly | 父子级选中不再关联 | boolean |
| \*fixedSelectLine | 只在多选模式下有效，用于控制选择框的行数，当行数过多时出现滚动条 true\|false，固定一行\|最高 4.5 行 | boolean | `false` |  |
### Option
```typescript
interface Option {
  value: string | number;
  label?: string | number;
  disabled?: boolean;
  children?: Option[];
  // 标记是否为叶子节点，设置了 `loadData` 时有效
  // 设为 `false` 时会强制标记为父节点，即使当前节点没有 children，也会显示展开图标
  isLeaf?: boolean;
}
```
> 注意，如果需要获得中国省市区数据，可以参考 [china-division](https://gist.github.com/afc163/7582f35654fd03d5be7009444345ea17)。
