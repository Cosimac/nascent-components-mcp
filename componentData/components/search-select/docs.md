标题显示在选择器内，其余能力与[选择器](/components/select)一致。
此处只做筛选区 UI 展示，具体功能请前往[选择器](/components/select)查看。
## 应用
- 用于列表筛选区。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E4%B8%8B%E6%8B%89%E9%80%89%E6%8B%A9%E5%99%A8)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#p21)
## 相关组件
- [选择器](/components/select)
## API
标题属性请参考 [GlobalTitle](/components/global-title/#API)，选择器属性请参考 [Select](/components/select/#API)。
> 注意，如果发现下拉菜单跟随页面滚动，或者需要在其他弹层中触发 Select，请尝试使用 `getPopupContainer={triggerNode => triggerNode.parentElement}` 将下拉弹层渲染节点固定在触发器的父元素中。
