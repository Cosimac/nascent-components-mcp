便于用户快速定位目标信息位置。
## 应用
- 页面信息过多时，（多组信息编辑页、数据展示页），可用该组件进行快速定位。
## 相关地址
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/%E6%AD%A5%E9%AA%A4%E6%9D%A1%E5%AE%9A%E4%BD%8D%E5%99%A8%E5%92%8C%E5%AE%9A%E4%BD%8D%E5%99%A8-UI/#s1)
## API
### Locator
| 参数      | 说明           | 类型                 | 默认值 | 版本 |
| --------- | -------------- | -------------------- | ------ | ---- |
| activeKey | 激活定位器 Key | `string` \| `number` | -      |      |
| options   | 定位器配置项   | [Options](#Options)  | -      |      |
| onClick   | 定位器切换响应 | function(e)          | -      |      |
| position  | 定位器方向     | `left` \| `right`    | left   |      |
### Options
| 参数   | 说明 | 类型                 | 默认值  | 版本 |
| ------ | ---- | -------------------- | ------- | ---- |
| key    | key  | `string` \| `number` |         |      |
| title  | 标题 | string               |         |      |
| status | 状态 | `default` \| `error` | default |      |
