轻量化信息提示，用于描述被指向的对象文字信息的气泡浮层。鼠标移入则显示提示，移出消失，气泡浮层不承载复杂文本和操作。
## 应用
鼠标移入则显示提示，移出消失，气泡浮层不承载复杂文本和操作。
可用来代替系统默认的 `title` 提示，提供一个 `按钮/文字/操作` 的文案解释。
用于文本/操作的解释说明。
## 文案
- 解释说明类文字提示：建议文案精简。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E6%96%87%E5%AD%97%E6%8F%90%E7%A4%BA)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s14)
## API
| 参数  | 说明     | 类型                         | 默认值 |
| ----- | -------- | ---------------------------- | ------ |
| title | 提示文字 | ReactNode \| () => ReactNode | -      |
### 共同的 API
以下 API 为 Tooltip、Popconfirm、Popover 共享的 API。
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| align | 该值将合并到 placement 的配置中，设置参考 [rc-tooltip](https://github.com/react-component/tooltip) | object | - |  |
| arrowPointAtCenter | 箭头是否指向目标元素中心 | boolean | true |  |
| autoAdjustOverflow | 气泡被遮挡时自动调整位置 | boolean | true |  |
| color | 背景颜色 | string | - | 4.3.0 |
| defaultVisible | 默认是否显隐 | boolean | false |  |
| destroyTooltipOnHide | 关闭后是否销毁 Tooltip，当 `keepParent` 为 `false` 时销毁父容器 | boolean \| { keepParent?: boolean } | false |  |
| getPopupContainer | 浮层渲染父节点，默认渲染到 body 上 | function(triggerNode) | () => document.body |  |
| mouseEnterDelay | 鼠标移入后延时多少才显示 Tooltip，单位：秒 | number | 0.1 |  |
| mouseLeaveDelay | 鼠标移出后延时多少才隐藏 Tooltip，单位：秒 | number | 0.1 |  |
| overlayClassName | 卡片类名 | string | - |  |
| overlayStyle | 卡片样式 | object | - |  |
| placement | 气泡框位置，可选 `top` `left` `right` `bottom` `topLeft` `topRight` `bottomLeft` `bottomRight` `leftTop` `leftBottom` `rightTop` `rightBottom` | string | `top` |  |
| trigger | 触发行为，可选 `hover` \| `focus` \| `click` \| `contextMenu`，可使用数组设置多个触发行为 | string \| string\[] | `hover` |  |
| visible | 用于手动控制浮层显隐 | boolean | false |  |
| zIndex | 设置 Tooltip 的 `z-index` | number | - |  |
| onVisibleChange | 显示隐藏的回调 | (visible) => void | - |  |
## 注意
请确保 `Tooltip` 的子元素能接受 `onMouseEnter`、`onMouseLeave`、`onFocus`、`onClick` 事件。
