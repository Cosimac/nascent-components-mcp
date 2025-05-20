空状态时的展示占位图。
## 应用
- 因无数据、无网络等造成的内容显示缺失时，给予用户提示
- 未配置插图用法时，支持适配宽度超过 700 像素时，显示为插图，否则显示为图标模式
## 文案
- 文案在简洁的同时，注意友好性。
- 面向 B 端用户时，不建议过多使用敬语，便于快速获取有效信息。
- 面对 C 端用户时，注意友好性，拉近用户距离，安抚负面情绪，例如：`抱歉…`。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E7%A9%BA%E7%8A%B6%E6%80%81)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s22)
## API
```jsx
<Empty>
  <Button>创建</Button>
</Empty>
```
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| description | 自定义描述内容 | ReactNode | - |  |
| image | 设置显示图片，为 string 时表示自定义图片地址。 | ReactNode | `Empty.PRESENTED_IMAGE_DEFAULT` |  |
| imageStyle | 图片样式 | CSSProperties | - |  |
