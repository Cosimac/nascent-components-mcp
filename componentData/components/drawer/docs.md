屏幕边缘滑出的浮层面板。
## 何时使用
需要用户处理事务，又不希望跳转页面以致打断工作流程时，可以使用 Drawer 在当前页面正中打开一个浮层，承载相应的操作。
当需要一个附加的面板来承载父窗体内容，这个面板在需要时呼出。
与【对话框】应用区别：
1. 需要承载更多信息和操作时，例如信息大于某个高度时，使用抽屉；
2. 需要对照父级页面信息/切换父级页面信息时，使用抽屉；
3. 需要阻断当前流程，优先用户进行交互行为时，使用对话框；抽屉干扰性<对话框；
4. 当需要承载表单场景时，使用对话框；信息过多可使用半页面对话框->全屏弹窗->页面；
5. 当需要承载展示信息时，优先考虑抽屉，可根据前 3 条，判断是否使用对话框；若信息内容过少，可直接使用【气泡】承载；
## 相关地址
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#p49)
## 复杂内容实现方式
若头部、主体、底部需要展示复杂内容，则传入 Drawer 内置的子组件或另外封装的组件的方式：
1. 根据需求调整对应区块样式，如头部无需内置间距，则在 headerStyle 手动去除样式；
2. 根据需求选择对应场景的子组件，传入区块。
## API
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| afterVisibleChange | 切换抽屉时动画结束后的回调 | function(visible) | - |  |
| bodyStyle | 可用于设置 Drawer 内容部分的样式 | CSSProperties | - |  |
| className | 对话框外层容器的类名 | string | - |  |
| closable | 是否显示右上角的关闭按钮 | boolean | true |  |
| closeIcon | 自定义关闭图标 | ReactNode | &lt;CloseOutlined /> |  |
| contentWrapperStyle | 可用于设置 Drawer 包裹内容部分的样式 | CSSProperties | - |  |
| destroyOnClose | 关闭时销毁 Drawer 里的子元素 | boolean | false |  |
| drawerStyle | 用于设置 Drawer 弹出层的样式 | CSSProperties | - |  |
| footer | 抽屉的页脚 | ReactNode | - |  |
| footerStyle | 抽屉页脚部件的样式 | CSSProperties | - |  |
| forceRender | 预渲染 Drawer 内元素 | boolean | false |  |
| getContainer | 指定 Drawer 挂载的 HTML 节点, false 为挂载在当前 dom | HTMLElement \| () => HTMLElement \| Selectors \| false | body |  |
| headerStyle | 用于设置 Drawer 头部的样式 | CSSProperties | - |  |
| height | 高度, 在 `placement` 为 `top` 或 `bottom` 时使用 | string \| number | 256 |  |
| keyboard | 是否支持键盘 esc 关闭 | boolean | true |  |
| mask | 是否展示遮罩 | boolean | false |  |
| maskClosable | 点击蒙层是否允许关闭 | boolean | true |  |
| maskStyle | 遮罩样式 | CSSProperties | {} |  |
| placement | 抽屉的方向 | `top` \| `right` \| `bottom` \| `left` | `right` |  |
| push | 用于设置多层 Drawer 的推动行为 | boolean \| { distance: string \| number } | { distance: 180 } | 4.5.0+ |
| size | 宽度尺寸，在 `placement` 为 `left` 或 `right` 时使用 | `small` \| `middle` \| `large` | - |  |
| style | 可用于设置 Drawer 最外层容器的样式，和 `drawerStyle` 的区别是作用节点包括 `mask` | CSSProperties | - |  |
| title | 标题 | ReactNode | - |  |
| visible | Drawer 是否可见 | boolean | - |  |
| width | 宽度 | string \| number | 256 |  |
| zIndex | 设置 Drawer 的 `z-index` | number | 1000 |  |
| onClose | 点击遮罩层或右上角叉或取消按钮的回调 | function(e) | - |  |
| \*\*drawerRender | 自定义渲染抽屉 | (node: ReactNode) => ReactNode | - |  |
| \*\*footer | 自定义底部内容 | ReactNode | - |  |
## Drawer.Information
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| title | 标题内容 | `string` | - | - |
| subTitle | 副标题内容,位于标题内容右侧 | `ReactNode` | - | - |
| description | 描述内容,位于标题内容的下方 | `string` | - | - |
| toolbar | 操作区展示，位于标题区域的右侧 | `ReactNode` | - | - |
| layout | 内容所占栅格数 | [LayoutProps](http://192.168.1.24:8024/components/drawer-cn/#LayoutProps/) | - | - |
## Drawer.Breadcrumb
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- | --- |
| onBack | 返回按钮的点击事件 | `() => (void | Promise)` | - | - |
| toolbar | 操作区展示，位于标题区域的右侧 | `ReactNode` | - | - |
| layout | 内容所占栅格数 | [LayoutProps](http://192.168.1.24:8024/components/drawer-cn/#LayoutProps/) | - | - |
更多属性请参考[BreadcrumbAutosize](http://192.168.1.24:8024/components/breadcrumb-autosize-cn/)
## LayoutProps
| 参数    | 说明               | 类型     | 默认值 | 版本 |
| ------- | ------------------ | -------- | ------ | ---- |
| main    | 主体部分所占栅格数 | `number` | 12     | -    |
| toolbar | 操作区所占栅格数   | `number` | 12     | -    |
