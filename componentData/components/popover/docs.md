---
category: Components
subtitle: 气泡卡片
type: 数据展示
title: Popover
cover: https://gw.alipayobjects.com/zos/alicdn/1PNL1p_cO/Popover.svg
cols: 1
---

Popover 以卡片的形式承载了更多的内容，比如链接、表单、按钮等。

## 何时使用

- 当触发组件有进一步的描述和相关操作时，可以收纳到卡片中，根据用户的操作行为进行展现。
- 和 [Tooltip（文字提示）](/components/tooltip) 的区别是，用户可以对浮层上的元素进行操作，因此它可以承载更复杂的内容，比如链接或按钮等。

## 相关地址

- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E6%B0%94%E6%B3%A1%E5%8D%A1%E7%89%87)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#p15)

## API

| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| content | 卡片内容 | ReactNode \| () => ReactNode | - |  |
| title | 卡片标题 | ReactNode \| () => ReactNode | - |  |
| \*\*footer | 卡片底部 | ReactNode \| () => ReactNode | - |  |
| \*\*size | 卡片尺寸 | `middle` \| `small` | `middle` |  |
| \*placement | 气泡框位置，可选 `top` `left` `right` `bottom` `topLeft` `topRight` `bottomLeft` `bottomRight` `leftTop` `leftBottom` `rightTop` `rightBottom` | string | `bottomLeft` |  |

更多属性请参考 [Tooltip](/components/tooltip/#API)。

## 注意

请确保 `Popover` 的子元素能接受 `onMouseEnter`、`onMouseLeave`、`onFocus`、`onClick` 事件。
