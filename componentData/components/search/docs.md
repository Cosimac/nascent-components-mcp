用于搜索场景。联想结果方便用户查看。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E6%90%9C%E7%B4%A2)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s20)
## 文案
1. 默认提示：`xx/xx`， 例如：`区域/店铺`；
2. 若无明显指示维度则显示`搜索…`。
## API
### Search
| 参数 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- | --- |
| value | 选中值 | string \| string[] |  |
| closeAfterSelect | 选中后是否关闭浮层，若`tab`中有配置则以 tab 为准 | boolean | true |
| tab | 多面板配置 | SearchGroup[] |  |
| multiple | 多选模式 | boolean | false |
| halfChecked | 多选模式下，半选状态集合 | string[] |  |
| checkAll | 多选模式下，是否可全选 | boolean |  |
| options | 选项数据 | `SearchOption[]` | - |
| dataSource | 本地搜索数据源 | `[]` | - |
| style | --- | React.CSSProperties | - |
| className | --- | string | - |
| size | 自定义三种尺寸 | `large` \| `middle` \| `small` | `middle` |
| dropdownClassName | 下拉菜单的 className 属性 | string | - |
| dropdownMatchSelectWidth | 下拉菜单和选择器同宽。默认将设置 min-width，当值小于选择框宽度时会被忽略。 | true \| number | true |
| getPopupContainer | 菜单渲染父节点。默认渲染到 body 上，如果你遇到菜单滚动定位问题，试试修改为滚动的区域，并相对其定位。[示例](https://codepen.io/afc163/pen/zEjNOy?editors=0010) | function(triggerNode) | () => document.body |
| placeholder | - | string |  |
| loading | 加载中 | boolean | false |
| optionRender | 搜索项自定义结构 | `ReactNode` | - |
| onChange | 选中的回调 | function(value, oldVal, changeVal) | - |
| onSearch | 搜索的回调 | function(searchValue) | - |
| labelHasLevel | 选项展示方式是否为多层级，开启时，数据需要存在`level`字段 | `boolean` | `false` |
| \*bordered | 是否有边框 | `none` | - | 4.5.0 |
### SearchOption
| 参数     | 说明           | 类型    | 默认值 |
| -------- | -------------- | ------- | ------ |
| value    | 选项值         | string  |        |
| label    | 选项展示的文案 | string  |        |
| disabled | 选项是否禁用   | boolean |        |
### SearchGroup
与一级 API 重复的配置，以此为准。
| 参数             | 说明               | 类型             | 默认值 |
| ---------------- | ------------------ | ---------------- | ------ |
| value            | tab 值             | string           |        |
| label            | tab 标题           | ReactNode        |        |
| closeAfterSelect | 选中后是否关闭浮层 | boolean          | true   |
| multiple         | 多选模式           | boolean          | false  |
| optionRender     | 搜索项自定义结构   | `ReactNode`      | -      |
| options          | 选项数据           | `SearchOption[]` | -      |
#### Search.Input
| 参数        | 说明                                     | 类型                       | 默认值 |
| ----------- | ---------------------------------------- | -------------------------- | ------ |
| allowClear  | 可以点击清除图标删除内容                 | boolean                    | true   |
| bordered    | 是否有边框                               | `none`                     | -      |
| className   | -                                        | string                     | -      |
| placeholder | -                                        | string                     | 搜索…  |
| style       | -                                        | React.CSSProperties        | -      |
| trigger     | 搜索模式：实时或触发搜索，默认为实时搜索 | `none` \| `click`          | `none` |
| onSearch    | 触发搜索，或按下回车键时的回调           | function(value, dimension) | -      |
| onChange    | 搜索值或维度发现变化时，调用此函数       | function(value, dimension) | -      |
### Option
| 参数  | 说明     | 类型             | 默认值 | 版本 |
| ----- | -------- | ---------------- | ------ | ---- |
| label | 属性文本 | `string`         | -      |      |
| value | 属性值   | string \| number | -      |      |
## 方法
| 名称             | 描述         | 版本 |
| ---------------- | ------------ | ---- |
| 【待定】search() | 手动触发搜索 |      |
