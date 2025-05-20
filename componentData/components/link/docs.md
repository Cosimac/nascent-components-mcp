文字超链接。
## 用处
- 在文本、段落中文字使用添加链接效果时使用。
## API
支持原生 `a` 标签的所有配置，例如`href`、`target`，其余不同 API 如下
| 成员     | 说明         | 类型                           | 默认值   | 版本 |
| -------- | ------------ | ------------------------------ | -------- | ---- |
| type     | 类型         | `link` \| `text`               | `link`   |      |
| size     | 设置大小     | `large` \| `middle` \| `small` | `middle` |
| icon     | 设置图标组件 | `ReactNode`                    | -        |      |
| onClick  | 点击事件     | `e => void`                    | -        |      |
| disabled | 是否禁用状态 | `boolean`                      | -        |      |
| danger   | 是否警告状态 | `boolean`                      | -        |      |
