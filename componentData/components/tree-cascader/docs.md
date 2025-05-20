常用于快速选择 区域/视角  或 区域/门店 等相关结构的场景
## 应用
- 需要从一组带层级的关联关系的数据集合进行选择，例如区域/视角、选择门店/员工等。
- 从一个较大的数据集合中进行选择时，用多级分类进行分隔，方便选择。
- 比起 Select 组件，可以在同一个浮层中完成选择，有较好的体验。
## 相关地址
- [交互稿（UE 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/ECRP%E7%BB%84%E4%BB%B6-UE/#g=1&p=%E7%BA%A7%E8%81%94%E9%80%89%E6%8B%A9%E5%99%A8)
- [设计稿（UI 稿）地址](http://192.168.1.90/%E5%8D%97%E8%AE%AF%E7%BB%84%E4%BB%B6%E8%AE%BE%E8%AE%A1%E7%A8%BF/V3/ECRP%E7%BB%84%E4%BB%B6%E5%BA%93/%E7%BA%A7%E8%81%94%E9%80%89%E6%8B%A9%E5%99%A8-UI/)
## API
```jsx
<TreeCascader value={value} options={options} onChange={onChange} />
```
| 参数 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| allowClear | 是否支持清除 | boolean | true |  |
| bordered | 是否有边框 | boolean | true |  |
| clearIcon | 自定义的选择框清空图标 | ReactNode | - |  |
| className | 自定义类名 | string | - |  |
| defaultValue | 默认的选中项 | string\[] \| number\[] | \[] |  |
| disabled | 禁用 | boolean | false |  |
| getPopupContainer | 菜单渲染父节点。默认渲染到 body 上，如果你遇到菜单滚动定位问题，试试修改为滚动的区域，并相对其定位。[示例](https://codepen.io/afc163/pen/zEjNOy?editors=0010) | function(triggerNode) | () => document.body |  |
| open | 控制浮层显隐 | boolean | - |  |
| options | 可选项数据源 | \[ [Option](#Option) \] | - |  |
| placeholder | 输入框占位文本 | string | `请选择` |  |
| placement | 浮层预设位置 | `bottomLeft` `bottomRight` `topLeft` `topRight` | `bottomLeft` |  |
| search | 在选择框中显示搜索框 | boolean \| [SearchProps](#SearchProps) | true |  |
| size | 输入框大小 | `large` \| `middle` \| `small` | - |  |
| style | 自定义样式 | CSSProperties | - |  |
| suffixIcon | 自定义的选择框后缀图标 | ReactNode | - |  |
| value | 指定选中项 | string[]\ \| number[]\ | - |  |
| onChange | 选择完成后的回调 | (value) => void | - |  |
| onDropdownVisibleChange | 显示/隐藏浮层的回调 | (value) => void | - |  |
| displayRender | 选择后展示的渲染函数 | (value:string[] \| string[]) => ReactNode | label => label.join(`/`) | `multiple`: 4.18.0 |
### Option
```typescript
import type { TreeProps } from './Tree';
interface Option {
  type: 'tree' | 'flat'; //类型为 树结构或平级结构
  data: treeOption[] | flatOption[]
  loading?:{
    spinning?:boolean, //是否加载中
    delay?:number //延迟显示加载效果的时间（防止闪烁）
  }
  placeholder?: string
  treeConfig?: TreeProps & { //TreeProps参数查看树形组件
  onSelect?: (key: React.Key) => void
  }
  flatConfig?:flatConfigProps // 平级数据源配置
  changeOnSelect?:boolean // 选择即赋值，option最后一个对象不受该字段影响，选择必赋值
}
```
### treeOption
```typescript
interface treeOption {
  title: string | number
  key: string | number
  isLeaf?:boolean
  tags?: tagsProps[]
  children?: treeOption[]
  disabled?: boolean
}
```
### flatOption
```typescript
interface flatOption {
  title: string | number
  key: string | number
  tags?: tagsProps[]
  disabled?: boolean
}
```
### flatConfigProps
```typescript
type flatConfigProps = {
  onSelect?: (key: string | number) => void  // 平级选择回调
  loadData?:(key: string | number) => void   //平级滚动懒加载
  minimumBatchSize?: number  //配合loadData使用，批量展示数量 默认100（pageSize配置多少 这边就配置多少） 参考vVirtualList.InfiniteLoader
  threshold?: number  //配合loadData使用，取数据的阈值 默认50  参考vVirtualList.InfiniteLoader （配置为pageSize的1/2即可）
}
```
### SearchProps
```typescript
interface SearchProps {
  onSearch: (searchValue: number | string, treeId: any) => void
  loading?: boolean
  tabs?: []
  searchOptions?: [{ label: number | string, value: number | string, level: string[], disabled?: boolean,levelKeys:string[] | number[] }] | // levelKeys，value地址集合必传 用于选中后 将完整value地址onChange出去，
    [[{ label: number | string, value: number | string, level: string[], disabled?: boolean,levelKeys:string[] | number[] }]]
}
```
### TagsProps
```typescript
type tagsProps = {
  label: string
  value: string | number
  color: string
}
```
> 注意，如果需要获得中国省市区数据，可以参考 [china-division](https://gist.github.com/afc163/7582f35654fd03d5be7009444345ea17)。
