上下条数据切换。
## 概述
用于快速查看表格中上下条数据详情。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E5%88%86%E9%A1%B5)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/21%E8%BD%AE%E8%BF%AD%E4%BB%A3UI/)
## API
| 成员     | 说明           | 类型                                   | 默认值 | 版本 |
| -------- | -------------- | -------------------------------------- | ------ | ---- |
| tip      | 上下项文字提示 | \[string, string]                      | -      |      |
| disabled | 禁用上下项按钮 | \[boolean, boolean]                    | -      |      |
| onClick  | 点击回调       | (event, type:'prev' \| 'next') => void | -      |      |
