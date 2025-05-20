选项卡切换组件。
## 应用
同级区域将大块内容进行收纳和展现，便于用户快速获取目标信息整洁。
我们提供了四种样式；应用于不同场景。
- 基础用法：一级切换；可用容器顶部，也可用于容器内部；所切换内容处于页面/模块信息层级高层级。
- 标签式页签：二级切换；常伴随页面一级 tab 出现，不建议单独出现；所切换内容处于页面/模块信息层级中层级。
- 文本式页签：三级切换；常用于容器内部；所切换内容处于页面/模块信息层级低层级。
- 卡片式页签：常用于容器内部，也可用于容器顶部；可有效进行区块划分。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=tab%E6%A0%87%E7%AD%BE)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s25)
## API
### Tabs
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| activeKey | 当前激活 tab 面板的 key | string | - |  |
| addIcon | 自定义添加按钮 | ReactNode | - | 4.4.0 |
| animated | 是否使用动画切换 Tabs, 仅生效于 `tabPosition="top"` | boolean \| { inkBar: boolean, tabPane: boolean } | { inkBar: true, tabPane: false } |  |
| centered | 标签居中展示 | boolean | false | 4.4.0 |
| \*\*bordered | 标签是否显示下划线 | boolean | true |  |
| defaultActiveKey | 初始化选中面板的 key，如果没有设置 activeKey | string | `第一个面板` |  |
| hideAdd | 是否隐藏加号图标，在 `type="editable-card"` 时有效 | boolean | false |  |
| moreIcon | 自定义折叠 icon | ReactNode | &lt;EllipsisOutlined /> | 4.14.0 |
| renderTabBar | 替换 TabBar，用于二次封装标签头 | (props: DefaultTabBarProps, DefaultTabBar: React.ComponentClass) => React.ReactElement | - |  |
| size | 大小，提供 `large` `default` 和 `small` 三种大小 | string | `default` |  |
| tabBarExtraContent | tab bar 上额外的元素 | ReactNode \| {left?: ReactNode, right?: ReactNode} | - | object: 4.6.0 |
| tabBarGutter | tabs 之间的间隙 | number | - |  |
| tabBarStyle | tab bar 的样式对象 | object | - |  |
| tabPosition | 页签位置，可选值有 `top` `right` `bottom` `left` | string | `top` |  |
| \*type | 页签的基本样式，可选 `line`、`tag`、`text`、`card`、`editable-card` 类型 | string | `line` |  |
| onChange | 切换面板的回调 | function(activeKey) {} | - |  |
| onEdit | 新增和删除页签的回调，在 `type="editable-card"` 时有效 | (targetKey, action): void | - |  |
| onTabClick | tab 被点击的回调 | function(key: string, event: MouseEvent) | - |  |
| onTabScroll | tab 滚动时触发 | function({ direction: `left` \| `right` \| `top` \| `bottom` }) | - | 4.3.0 |
### Tabs.TabPane
| 参数        | 说明                                            | 类型      | 默认值 |
| ----------- | ----------------------------------------------- | --------- | ------ |
| closeIcon   | 自定义关闭图标，`在 type="editable-card"`时有效 | ReactNode | -      |
| forceRender | 被隐藏时是否渲染 DOM 结构                       | boolean   | false  |
| key         | 对应 activeKey                                  | string    | -      |
| tab         | 选项卡头显示文字                                | ReactNode | -      |
### Tabs.TabTitle
| 参数     | 说明               | 类型                     | 默认值 | 版本 |
| -------- | ------------------ | ------------------------ | ------ | ---- |
| title    | 标题内容           | string                   | 标题   |      |
| titleTip | 自定义标题解释内容 | ReactNode\|false         | false  |      |
| size     | 大小               | large \| middle \| small | middle |      |
| disabled | 是否禁用           | boolean                  | false  |      |
