引导用户按照流程完成任务的导航条。
## 应用
当任务复杂或者存在先后关系时，将其分解成一系列步骤，从而简化任务。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E6%AD%A5%E9%AA%A4%E6%9D%A1)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UI/#s43)
## API
```jsx
<Steps>
  <Step title="第一步" />
  <Step title="第二步" />
  <Step title="第三步" />
</Steps>
```
### Steps
整体步骤条。
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| className | 步骤条类名 | string | - |  |
| current | 指定当前步骤，从 0 开始记数。在子 Step 元素中，可以通过 `status` 属性覆盖状态 | number | 0 |  |
| direction | 指定步骤条方向。目前支持水平（`horizontal`）和竖直（`vertical`）两种方向 | string | `horizontal` |  |
| initial | 起始序号，从 0 开始记数 | number | 0 |  |
| labelPlacement | 指定标签放置位置，默认水平放图标右侧，可选 `vertical` 放图标下方 | string | `horizontal` |  |
| percent | 当前 `process` 步骤显示的进度条进度（只对基本类型的 Steps 生效） | number | - | 4.5.0 |
| progressDot | 点状步骤条，可以设置为一个 function，labelPlacement 将强制为 `vertical` | boolean \| (iconDot, {index, status, title, description}) => ReactNode | false |  |
| responsive | 当屏幕宽度小于 532px 时自动变为垂直模式 | boolean | - | true |
| size | 指定大小，目前支持普通（`default`）和迷你（`small`） | string | `default` |  |
| status | 指定当前步骤的状态，可选 `wait` `process` `finish` `error` | string | `process` |  |
| type | 步骤条类型，有 `default` 和 `navigation` 两种 | string | `default` |  |
| gradually | 是否渐进式，一步一步往下走，可回切完成的步骤，不能够跳步骤 | boolean | false |
| onChange | 点击切换步骤时触发 | (current) => void | - |  |
### Steps.Step
步骤条内的每一个步骤。
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| description | 步骤的详情描述，可选 | ReactNode | - |  |
| disabled | 禁用点击 | boolean | false |  |
| icon | 步骤图标的类型，可选 | ReactNode | - |  |
| status | 指定状态。当不配置该属性时，会使用 Steps 的 `current` 来自动指定状态。可选：`wait` `process` `finish` `error` | string | `wait` |  |
| subTitle | 子标题 | ReactNode | - |  |
| title | 标题 | ReactNode | - |  |
## FAQ
### 如何动态增删步骤条？
可通过在更新数据的时候对组件进行销毁渲染从而达到动态增删步骤条的效果
