## 应用
- 用于列表筛选区。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/%E5%AF%BC%E5%85%A5%E6%90%9C%E7%B4%A2-UI/)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/%E5%AF%BC%E5%85%A5%E6%90%9C%E7%B4%A2-UI/)
## 相关组件
- [选择器](/components/select)
## API
### SearchImport props
| 参数               | 说明 | 类型 | 默认值 | 版本 |
|------------------| --- | --- | --- | --- |
| value            | 值 | [ValueProps](/components/search-import#ValueProps) | - |  |
| defaultValue     | 指定默认值 | `ValueProps` | - |  |
| disabled         | 是否禁用 | boolean | false |  |
| leftOptions      | 左侧-下拉菜单配置 | `Option[]` | - |  |
| leftSelectExtend | 左侧下拉的原始参数扩展 | [Select props](/components/select/#API) | - | 3.5.41 |
| selectOptions    | 当值为数组时的下拉菜单配置 | `Option[]` | - |  |
| rightButtons     | 右侧按钮配置 | `RightButtons[]` | - |  |
| rightClick       | 点击右侧 Icon 或者下拉按钮组调用此函数 | function(e: {key: string}) | - |  |
| placeholder      | 选择框默认文本 | string | - |  |
| size             | 选择框大小 | `large` \| `middle` \| `small` | `middle` |  |
| trigger          | 触发 onChange | `click` |  |  |
| onBlur           | 失去焦点时回调\|多个地方触发此事件 | function(value: ValueProps) | - |  |
| onChange         | 左侧下拉 或 input 的 value 变化时，调用此函数 | function(value: ValueProps) | - |  |
| onSearch         | trigger 为 click 时，点击右侧搜索 Icon 按钮时，调用此函数 | function(value: ValueProps) | - |  |
| allowValue       | 输入框输入的值是否被允许 | function(value: ValueProps) | - | 3.7.7  |
| popoverProps     | 浮层参数透传 | `Object` | - | 3.7.7 |
> 注意，默认宽度 240px 或 330px（有 title 或者左侧下拉的情况）。可自定义 style
## ValueProps
| 参数      | 说明                             | 类型             | 默认值 | 版本 |
| --------- | -------------------------------- | ---------------- | ------ | ---- |
| value     | 值                               | any              | -      |      |
| leftValue | 左侧下拉值-配置 leftOptions 才有 | string \| number | -      |      |
| type      | 值                               | string \| number | -      |      |
### ValueProps , Option , RightButtons
```typescript
import { ValueProps, Option, RightButtons } from '@nascent/nui/lib/search-import';
type ValueProps = {
  leftValue: string | number;
  value: any;
  type: string | number; //右侧下拉按钮的key。
};
interface Option {
  disabled?: boolean | undefined;
  label: string;
  value: string | number;
}
interface RightButtons {
  title: string;
  key: string;
}
```
