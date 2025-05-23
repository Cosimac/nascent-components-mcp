点击元素，弹出气泡式的确认框。
## 应用
目标元素的操作需要用户进一步的确认时，在目标元素附近弹出浮层提示，询问用户。
和 `confirm` 弹出的全屏居中模态对话框相比，交互形式更轻量。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E6%B0%94%E6%B3%A1%E7%A1%AE%E8%AE%A4%E6%A1%86)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#p31)
## API
| 参数 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| cancelButtonProps | cancel 按钮 props | [ButtonProps](/components/button/#API) | - |
| cancelText | 取消按钮文字 | string | `取消` |
| disabled | 阻止点击 Popconfirm 子元素时弹出确认框 | boolean | false |
| icon | 自定义弹出气泡 Icon 图标 | ReactNode | &lt;ExclamationCircle /> |
| okButtonProps | ok 按钮 props | [ButtonProps](/components/button/#API) | - |
| okText | 确认按钮文字 | string | `确定` |
| okType | 确认按钮类型 | string | `primary` |
| title | 确认框的描述 | ReactNode \| () => ReactNode | - |
| onCancel | 点击取消的回调 | function(e) | - |
| onConfirm | 点击确认的回调 | function(e) | - |
更多属性请参考 [Tooltip](/components/tooltip/#API)。
## 注意
请确保 `Popconfirm` 的子元素能接受 `onMouseEnter`、`onMouseLeave`、`onFocus`、`onClick` 事件。
