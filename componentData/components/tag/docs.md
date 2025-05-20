对不同维度进行简单的标记和分类。
## 应用
- 用于标记事物的属性和维度。
- 进行分类，便于搜索查询。
## 文案
- 描述文字应选关键词，保持简洁。
## 相关地址
- 标签
  - [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E6%A0%87%E7%AD%BE)
  - [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s19)
- 标签组
  - [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/%E6%A0%87%E7%AD%BE-UI/)
## API
### Tag
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| closable | 标签是否可以关闭（点击默认关闭） | boolean | false |  |
| closeIcon | 自定义关闭按钮 | ReactNode | - | 4.4.0 |
| color | 标签色 | string | - |  |
| icon | 设置图标 | ReactNode | - |  |
| visible | 是否显示标签 | boolean | true |  |
| onClose | 关闭时的回调（可通过 `e.preventDefault()` 来阻止默认行为） | (e) => void | - |  |
| \*\*size | 设置标签大小 | `large` \| `middle` \| `small` | `middle` |  |
| \*\*disabled | 标签失效状态 | boolean | false |  |
| \*\*allowTooltip | 当文本过长时，用于手动控制是否显示省略提示 | boolean | true |  |
| \*\*confirm | 标签可关闭时，是否需要二次确认 | boolean \| (ReactNode:React.ReactNode) => React.ReactNode | true |  |
| \*\*checked | 设置标签的选中状态 | boolean | false |
| \*\*onChange | 点击标签时触发的回调 | (checked) => void | - |
| \*\*forbidden | 标签禁用状态 | [ConfirmProps](#confirmprops) | false |  |
### Tag Group
父容器需存在宽度（百分比和固定值均可），否则组件会渲染异常。
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| options | 标签组 | [GroupOption](#GroupOption)\[] | [] |  |
| maxRows | 展示层最大行数 | number | 3 |  |
| size | 标签组标签大小 | `large` \| `middle` \| `small` | `middle` |  |
| title | 缩略气泡展示 标题（必填，否则无法使用） | string |  |  |
| onChange | 选择回调 | (tag,checked)=> void |  |  |
| popoverRender | 自定义展开内容 | (node: ReactNode) => ReactNode |  |  |
#### GroupOption
```typescript
interface GroupOption {
  label: string | number;
  value: string | number;
  closable?: boolean;
  closeIcon?: ReactNode;
  color?: string;
  icon?: ReactNode;
  visible?: boolean;
  disabled?: boolean;
  confirm?: (ReactNode: React.ReactNode) => React.ReactNode | boolean;
  checked?: boolean;
}
```
