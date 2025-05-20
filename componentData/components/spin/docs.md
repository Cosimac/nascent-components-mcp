页面局部处于等待异步数据或正在渲染过程时，合适的加载动效会有效缓解用户的焦虑。
## 应用
用于页面或者区块的加载状态，如：页面加载，列表加载，按钮等待，全局加载中
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E5%8A%A0%E8%BD%BD)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s23)
## API
| 参数             | 说明                                         | 类型               | 默认值    |
| ---------------- | -------------------------------------------- | ------------------ | --------- |
| delay            | 延迟显示加载效果的时间（防止闪烁）           | `number (毫秒)`    | -         |
| indicator        | 加载指示符                                   | `ReactNode`        | -         |
| size             | 组件大小，可选值为 `small` `default` `large` | `string`           | `default` |
| spinning         | 是否为加载中状态                             | `boolean`          | true      |
| tip              | 当作为包裹元素时，可以自定义描述文案         | `string`           | -         |
| wrapperClassName | 包装器的类属性                               | `string`           | -         |
| \*\*image        | 自定义加载中图片                             | `string` \| `null` | -         |
### 静态方法
- `Spin.setDefaultIndicator(indicator: ReactNode)`
  你可以自定义全局默认 Spin 的元素。
