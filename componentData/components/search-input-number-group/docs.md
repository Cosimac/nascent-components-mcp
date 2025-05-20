标题显示在选择器内，其余能力与[树选择](/components/tree-select)一致。
此处只做筛选区 UI 展示，具体功能请前往[树选择](/components/tree-select)查看。
## 应用
- 用于列表筛选区。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E6%95%B0%E5%AD%97%E8%BE%93%E5%85%A5%E6%A1%86)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s33)
## 相关组件
- [数字输入框](/components/input-number)
## API
标题显示在输入框内，其余能力与[InputNumber](/components/input-number)一致。
## SearchInputNumberProps
| 参数     | 说明                     | 类型                           | 默认值   | 版本 |
| -------- | ------------------------ | ------------------------------ | -------- | ---- |
| size     | 自定义数字输入框三种尺寸 | `large` \| `middle` \| `small` | `middle` |      |
| title    | 自定义数字输入框标题名称 | `string`                       |          |      |
| titleTip | 自定义数字输入框题提示   | `ReactNode` \| `false`         | `false`  |      |
标题属性请参考 [GlobalTitle](/components/global-title/#API)，数字输入框属性请参考 [InputNumber](/components/input-number/#API)。
