复选框允许用户从可见列表中选择一个或多个选项。
## 应用
- 当用户需要进行多项选择时；多用于表格中。
- 用于表单新建、编辑场景, 4 个层级以内的数据选择，如果选项大于 4 个，建议使用下拉选择器。特殊情况除。
- 单独使用可以表示两种状态之间的切换，和 switch 类似。区别在于切换 switch 会直接触发状态改变，而 checkbox 一般用于状态标记，需要和提交操作配合。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E5%A4%8D%E9%80%89)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s11)
## API
### 属性
#### Checkbox
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| autoFocus | 自动获取焦点 | boolean | false |  |
| checked | 指定当前是否选中 | boolean \| string \| number | false |  |
| defaultChecked | 初始是否选中 | boolean \| string \| number | false |  |
| disabled | 失效状态 | boolean | false |  |
| indeterminate | 设置 indeterminate 状态，只负责样式控制 | boolean | false |  |
| onChange | 变化时回调函数 | function(e:Event) | - |  |
| \*\*checkedValue | 选中时的值 | boolean \| string \| number | true |  |
| \*\*unCheckedValue | 未选中时的值 | boolean \| string \| number | false |  |
#### Checkbox.Group
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| defaultValue | 默认选中的选项 | string\[] | \[] |  |
| disabled | 整组失效 | boolean | false |  |
| name | CheckboxGroup 下所有 `input[type="checkbox"]` 的 `name` 属性 | string | - |  |
| options | 指定可选项 | string\[] \| Option\[] | \[] |  |
| value | 指定选中的选项 | string\[] | \[] |  |
| onChange | 变化时回调函数 | function(checkedValue) | - |  |
| \*\*direction | 复选框组合排列方式,可选值有`horizontal` `vertical` | string | `horizontal` |  |
| \*\*clickArea | 复选框组合垂直排列时单选框点击范围,可选值有`text` `all` | string | `text` |  |
| \*\*allowTooltip | 当文本过长时，用于手动控制是否显示省略提示 | boolean | true |  |
##### Option
```typescript
interface Option {
  label: string;
  value: string;
  disabled?: boolean;
}
```
### 方法
#### Checkbox
| 名称    | 描述     | 版本 |
| ------- | -------- | ---- |
| blur()  | 移除焦点 |      |
| focus() | 获取焦点 |      |
