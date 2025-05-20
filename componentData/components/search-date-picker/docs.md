标题显示在选择器内，其余能力与[日期选择器](/components/date-picker)一致。
此处只做筛选区 UI 展示，具体功能请前往[日期选择器](/components/date-picker)查看。
## 应用
- 用于列表筛选区。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E5%BC%80%E5%85%B3)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s27)
## 相关组件
- [日期选择器](/components/date-picker)
## API
## SearchDatePickerProps
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| size | 自定义日期选择器三种尺寸 | `large` \| `middle` \| `small` | `middle` |  |
| title | 自定义日期选择器标题名称 | string |  |  |
| titleTip | 自定义日期选择器标题提示 | `ReactNode` \| `false` | `false` |  |
| isRange | 是否是范围选择器 | boolean | `false` |  |
| isDropdownFixLeft | 是否下拉面板固定在左侧 | boolean | `true` |  |
| outerRanges | 自定义维度选择 | OuterRangesOption[] | `[]` |  |
| onChange | 时间发生变化的回调 | function(date: moment \| \[moment, moment], dateString: string \| \[string, string]) | - |  |
支持配置日期选择器其他属性，日期选择器属性请参考 [DatePicker](/components/date-picker/#API)
## OuterRangesOption
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| title | 自定义维度名称 | string |  |  |
| match | 自定义维度匹配规则，如果是范围选择器需要传入包含两个时间点的数组 | `Moment` \| ()=> Moment \| `[Moment, Moment]` \| ()=> \[Moment, Moment] \| `undefined` \| `null` |  |  |
| key | React 需要用到的 key | string \| number |  |  |
### 方法
| 名称    | 描述     | 版本 |
| ------- | -------- | ---- |
| blur()  | 移除焦点 |      |
| focus() | 获取焦点 |      |
