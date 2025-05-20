需要表示开关状态/开启关闭两种状态之间的切换。
## 应用
- 常见于表格、表单场景，用于快速切换数据状态；
- 和 `checkbox` 的区别是，切换 `switch` 会直接触发状态改变，而 `checkbox` 一般用于状态标记，需要和提交操作配合。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E5%BC%80%E5%85%B3)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#p35)
## API
| 参数 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| autoFocus | 组件自动获取焦点 | boolean | false |
| checked | 指定当前是否选中 | boolean \| string \| number | false |
| checkedChildren | 选中时的内容 | ReactNode | - |
| className | Switch 器类名 | string | - |
| defaultChecked | 初始是否选中 | boolean \| string \| number | false |
| disabled | 是否禁用 | boolean | false |
| loading | 加载中的开关 | boolean | false |
| size | 开关大小，可选值：`default` `large` | string | `default` |
| \*\*description | 描述信息 | ReactNode \| string | - |
| unCheckedChildren | 非选中时的内容 | ReactNode | - |
| onChange | 变化时回调函数 | function(checked: boolean \| string \| number, event: Event) | - |
| onClick | 点击时回调函数 | function(checked: boolean \| string \| number, event: Event) | - |
| \*\*checkedValue | 选中时的值 | boolean \| string \| number | true |
| \*\*unCheckedValue | 未选中时的值 | boolean \| string \| number | false |
## 方法
| 名称    | 描述     |
| ------- | -------- |
| blur()  | 移除焦点 |
| focus() | 获取焦点 |
