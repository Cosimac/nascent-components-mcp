选择（也可进行输入定位）日期的控件。
## 应用
当用户需要输入一个日期，可以点击标准输入框，弹出日期面板进行选择。
## 文案
- 基础：请选择日期/请选择周/请选择月。
- 起止：开始时间，结束时间。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E6%97%A5%E6%9C%9F%E6%97%B6%E9%97%B4%E9%80%89%E6%8B%A9%E5%99%A8)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/%E6%97%A5%E6%9C%9F%E9%80%89%E6%8B%A9%E5%99%A8-UI/)
## 相关组件
- [筛选区日期选择器](/components/search-date-picker)
- [时间选择器](/components/time-picker)
## API
日期类组件包括以下五种形式。
- DatePicker
- DatePicker\[picker="month"]
- DatePicker\[picker="week"]
- DatePicker\[picker="year"]
- DatePicker\[picker="quarter"]
- RangePicker
### 国际化配置
默认配置为 zh-CN，如果你需要设置其他语言，推荐在入口处使用我们提供的国际化组件，详见：[ConfigProvider 国际化](http://192.168.1.24:8024/components/config-provider-cn/)。
如有特殊需求（仅修改单一组件的语言），请使用 locale 参数，参考：[默认配置](https://github.com/ant-design/ant-design/blob/master/components/date-picker/locale/example.json)。
```jsx
import 'moment/locale/zh-cn';
import locale from '@nascent/nui/es/date-picker/locale/zh_CN';
<DatePicker locale={locale} />;
```
```jsx
// 默认语言为 zh-CN，如果你需要设置其他语言，推荐在入口文件全局设置 locale
import moment from 'moment';
import 'moment/locale/en-us';
import locale from '@nascent/nui/lib/locale/en_US';
<ConfigProvider locale={locale}>
  <DatePicker defaultValue={moment('2015-01-01', 'YYYY-MM-DD')} />
</ConfigProvider>;
```
### 共同的 API
以下 API 为 DatePicker、 RangePicker 共享的 API。
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| allowClear | 是否显示清除按钮 | boolean | true |  |
| autoFocus | 自动获取焦点 | boolean | false |  |
| className | 选择器 className | string | - |  |
| dateRender | 自定义日期单元格的内容 | function(currentDate: moment, today: moment) => React.ReactNode | - |  |
| disabled | 禁用 | boolean | false |  |
| disabledDate | 不可选择的日期 | (currentDate: moment) => boolean | - |  |
| dropdownClassName | 额外的弹出日历 className | string | - |  |
| getPopupContainer | 定义浮层的容器，默认为 body 上新建 div | function(trigger) | - |  |
| inputReadOnly | 设置输入框为只读（避免在移动设备上打开虚拟键盘） | boolean | false |  |
| locale | 国际化配置 | object | [默认配置](https://github.com/ant-design/ant-design/blob/master/components/date-picker/locale/example.json) |  |
| mode | 日期面板的状态（[设置后无法选择年份/月份？](/docs/react/faq#当我指定了-DatePicker/RangePicker-的-mode-属性后，点击后无法选择年份/月份？)） | `time` \| `date` \| `month` \| `year` \| `decade` | - |  |
| open | 控制弹层是否展开 | boolean | - |  |
| panelRender | 自定义渲染面板 | (panelNode) => ReactNode | - |  |
| picker | 设置选择器类型 | `date` \| `week` \| `month` \| `quarter` \| `year` | `date` |  |
| placeholder | 输入框提示文字 | string \| \[string, string] | - |  |
| popupStyle | 额外的弹出日历样式 | CSSProperties | {} |  |
| size | 输入框大小，`large` 高度为 40px，`small` 为 24px，默认是 32px | `large` \| `middle` \| `small` | - |  |
| style | 自定义输入框样式 | CSSProperties | {} |  |
| suffixIcon | 自定义的选择框后缀图标 | ReactNode | - |  |
| onOpenChange | 弹出日历和关闭日历的回调 | function(open) | - |  |
| onPanelChange | 日历面板切换的回调 | function(value, mode) | - |  |
### 共同的方法
| 名称    | 描述     | 版本 |
| ------- | -------- | ---- |
| blur()  | 移除焦点 |      |
| focus() | 获取焦点 |      |
### DatePicker
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| defaultPickerValue | 默认面板日期 | [moment](http://momentjs.com/) | - |  |
| defaultValue | 默认日期，如果开始时间或结束时间为 `null` 或者 `undefined`，日期范围将是一个开区间 | [moment](http://momentjs.com/) | - |  |
| disabledTime | 不可选择的时间 | function(date) | - |  |
| format | 设置日期格式，为数组时支持多格式匹配，展示以第一个为准。配置参考 [moment.js](http://momentjs.com/)，支持[自定义格式](#components-date-picker-demo-format) | string \| (value: moment) => string \| (string \| (value: moment) => string)\[] | `YYYY-MM-DD` |  |
| renderExtraFooter | 在面板中添加额外的页脚 | (mode) => React.ReactNode | - |  |
| showNow | 当设定了 `showTime` 的时候，面板是否显示“此刻”按钮 | boolean | - |  |
| showTime | 增加时间选择功能 | Object \| boolean | [TimePicker Options](/components/time-picker/#API) |  |
| showTime.defaultValue | 设置用户选择日期时默认的时分秒，[例子](#components-date-picker-demo-disabled-date) | [moment](http://momentjs.com/) | moment() |  |
| showToday | 是否展示“今天”按钮 | boolean | true |  |
| value | 日期 | [moment](http://momentjs.com/) | - |  |
| onChange | 时间发生变化的回调 | function(date: moment, dateString: string) | - |  |
| onOk | 点击确定按钮的回调 | function() | - |  |
| onPanelChange | 日期面板变化时的回调 | function(value, mode) | - |  |
### DatePicker\[picker=year]
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| defaultPickerValue | 默认面板日期 | [moment](http://momentjs.com/) | - |  |
| defaultValue | 默认日期 | [moment](http://momentjs.com/) | - |  |
| format | 展示的日期格式，配置参考 [moment.js](http://momentjs.com/) | string | `YYYY` |  |
| renderExtraFooter | 在面板中添加额外的页脚 | () => React.ReactNode | - |  |
| value | 日期 | [moment](http://momentjs.com/) | - |  |
| onChange | 时间发生变化的回调，发生在用户选择时间时 | function(date: moment, dateString: string) | - |  |
### DatePicker\[picker=quarter]
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| defaultPickerValue | 默认面板日期 | [moment](http://momentjs.com/) | - |  |
| defaultValue | 默认日期 | [moment](http://momentjs.com/) | - |  |
| format | 展示的日期格式，配置参考 [moment.js](http://momentjs.com/) | string | `YYYY-\QQ` |  |
| renderExtraFooter | 在面板中添加额外的页脚 | () => React.ReactNode | - |  |
| value | 日期 | [moment](http://momentjs.com/) | - |  |
| onChange | 时间发生变化的回调，发生在用户选择时间时 | function(date: moment, dateString: string) | - |  |
### DatePicker\[picker=month]
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| defaultPickerValue | 默认面板日期 | [moment](http://momentjs.com/) | - |  |
| defaultValue | 默认日期 | [moment](http://momentjs.com/) | - |  |
| format | 展示的日期格式，配置参考 [moment.js](http://momentjs.com/) | string | `YYYY-MM` |  |
| monthCellRender | 自定义的月份内容渲染方法 | function(date, locale): ReactNode | - |  |
| renderExtraFooter | 在面板中添加额外的页脚 | () => React.ReactNode | - |  |
| value | 日期 | [moment](http://momentjs.com/) | - |  |
| onChange | 时间发生变化的回调，发生在用户选择时间时 | function(date: moment, dateString: string) | - |  |
### DatePicker\[picker=week]
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| defaultPickerValue | 默认面板日期 | [moment](http://momentjs.com/) | - |  |
| defaultValue | 默认日期 | [moment](http://momentjs.com/) | - |  |
| format | 展示的日期格式，配置参考 [moment.js](http://momentjs.com/) | string | `YYYY-wo` |  |
| renderExtraFooter | 在面板中添加额外的页脚 | (mode) => React.ReactNode | - |  |
| value | 日期 | [moment](http://momentjs.com/) | - |  |
| onChange | 时间发生变化的回调，发生在用户选择时间时 | function(date: moment, dateString: string) | - |  |
### RangePicker
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| allowEmpty | 允许起始项部分为空 | \[boolean, boolean] | \[false, false] |  |
| dateRender | 自定义日期单元格的内容 | function(currentDate: moment, today: moment, info: { range: `start` \| `end` }) => React.ReactNode | - |  |
| defaultPickerValue | 默认面板日期 | [moment](http://momentjs.com/)\[] | - |  |
| defaultValue | 默认日期 | [moment](http://momentjs.com/)\[] | - |  |
| disabled | 禁用起始项 | \[boolean, boolean] | - |  |
| disabledTime | 不可选择的时间 | function(date: moment, partial: `start` \| `end`) | - |  |
| format | 展示的日期格式 | string | `YYYY-MM-DD HH:mm:ss` |  |
| ranges | 预设时间范围快捷选择 | { \[range: string]: [moment](http://momentjs.com/)\[] } \| { \[range: string]: () => [moment](http://momentjs.com/)\[] } | - |  |
| renderExtraFooter | 在面板中添加额外的页脚 | () => React.ReactNode | - |  |
| separator | 设置分隔符 | React.ReactNode | `<SwapRightOutlined />` |  |
| showTime | 增加时间选择功能 | Object\|boolean | [TimePicker Options](/components/time-picker/#API) |  |
| showTime.defaultValue | 设置用户选择日期时默认的时分秒，[例子](#components-date-picker-demo-disabled-date) | [moment](http://momentjs.com/)\[] | \[moment(), moment()] |  |
| value | 日期 | [moment](http://momentjs.com/)\[] | - |  |
| onCalendarChange | 待选日期发生变化的回调 | function(dates: \[moment, moment], dateStrings: \[string, string], info: { range:`start`\|`end` }) | - |  |
| onChange | 日期范围发生变化的回调 | function(dates: \[moment, moment], dateStrings: \[string, string]) | - |  |
## FAQ
### 当我指定了 DatePicker/RangePicker 的 mode 属性后，点击后无法选择年份/月份？
请参考[常见问答](/docs/react/faq#当我指定了-DatePicker/RangePicker-的-mode-属性后，点击后无法选择年份/月份？)
### 如何在 DatePicker 中使用自定义日期库（如 dayjs ）？
请参考[《替换 Moment.js》](/docs/react/replace-moment#DatePicker)
### 为何全局修改 moment.locale 不生效？
DatePicker 默认 `locale` 为 `zh`。你可以通过 DatePicker 的 `locale` 属性来单独设置，也可以通过 [ConfigProvider `locale`](/components/config-provider) 属性来配置。
### 如何修改周的起始日？
请使用正确的[语言包](/docs/react/i18n)（[#5605](https://github.com/ant-design/ant-design/issues/5605)），或者修改 moment 的 `locale` 配置：<https://codesandbox.io/s/moment-day-of-week-6dby5>
### 为何使用 `panelRender` 时，原来面板无法切换？
当你通过 `panelRender` 动态改变层级结构时，会使得原本的 Panel 被当做新的节点删除并创建。这使得其原本的状态会被重置，保持结构稳定即可。详情请参考 [#27263](https://github.com/ant-design/ant-design/issues/27263)。
```js
moment.locale('en', {
  // 注意请修改你正在使用的 locale 语言，比如 en-us
  week: {
    dow: 1,
  },
});
```
