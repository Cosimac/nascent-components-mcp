标题显示在选择器内，其余能力与[时间选择器](/components/time-picker)一致。
此处只做筛选区 UI 展示，具体功能请前往[时间选择器](/components/time-picker)查看。
## 何时使用
当用户需要输入一个时间，可以点击标准输入框，弹出时间面板进行选择。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E5%BC%80%E5%85%B3)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s27)
## 相关组件
- [时间选择器](/components/time-picker)
## API
## SearchTimePickerProps
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| size | 自定义时间选择器三种尺寸 | `large` \| `middle` \| `small` | `middle` |  |
| title | 自定义时间选择器标题名称 | string |  |  |
| titleTip | 自定义时间选择器标题提示 | `ReactNode` \| `false` | `false` |  |
| isRange | 是否是范围选择器 | boolean | `false` |  |
| isDropdownFixLeft | 是否下拉面板固定在左侧 | boolean | `true` |  |
| outerRanges | 自定义维度选择 | OuterRangesOption[] | `[]` |  |
| onChange | 时间发生变化的回调 | function(date: moment \| \[moment, moment], dateString: string \| \[string, string]) | - |  |
支持配置时间选择器其他属性，请参考 [TimePicker](/components/time-picker/#API)
## OuterRangesOption
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| title | 自定义维度名称 | string |  |  |
| match | 自定义维度匹配规则，如果是范围选择器需要传入包含两个时间点的数组 | `Moment` \| ()=> Moment \| `[Moment, Moment]` \| ()=> \[Moment, Moment] |  |  |
| key | React 需要用到的 key | string \| number |  |  |
### 方法
| 名称    | 描述     | 版本 |
| ------- | -------- | ---- |
| blur()  | 移除焦点 |      |
| focus() | 获取焦点 |      |
