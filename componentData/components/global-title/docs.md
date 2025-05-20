标题组件主要用于对标题文字进行限制字数展示。
## 应用
- 需要控制显示字数，并对省略的文字需要文字提示时使用。
- 在各筛选区组件标题区使用。
- 对省略的文字提供解释说明。
## API
### GlobalTitle
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| title | 标题内容 | string | - |  |
| titleTip | 自定义标题解释内容 | ReactNode\|false | false |  |
| hasColon | 是否需要冒号 | boolean | true |  |
| size | 大小 | large \| middle \| small | middle |  |
| isFixLength | 是否固定文字宽度。默认文字宽度自适应，超出配置字符长度省略。设置为`true`时根据配置字符长度固定文字宽度，超出省略，与全局配置搭配使用，暂时用于 Form 表单 label | boolean | false |  |
