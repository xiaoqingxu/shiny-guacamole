## CSS规范
- 使用两个空格作为缩进
- 小写
- 使用BEM命名规则，即：`block__element--modifier`
    - 之所以使用连续两个连字符和下划线，是为了让自己的块可以用单个连字符来界定
    - block:模块
    - element：模块里边的元素
    - modifier：元素的不同状态或版本
    - 例子
    `.person__hand--left{}`

##JSX
 - 模块
    - 每个文件只写一个模块，多个无状态模块可以放在单个文件中。
    - 如果你的模块有内部状态或者是refs, 推荐使用 class extends React.Component 而不是React.createClass。
```javascript
class Listing extends React.Component {
  // ...
  render() {
    return <div>{this.state.hello}</div>;
  }
}
```
    - 如果你的模块没有状态或是没有引用refs， 推荐使用普通函数（非箭头函数）而不是类。
```
function Listing({ hello }) {
  return <div>{hello}</div>;
}
```
 - 命名
    - 扩展名: React模块使用 .jsx 扩展名.  
    - 模块文件和文件夹,驼峰命名,首字母大写,其余文件、文件夹名小写，
    - 模块命名: 模块内入口文件名为 Index.jsx 
```
import ReservationCard from './ReservationCard';
const reservationItem = <ReservationCard />;
```
    - 属性命名: 避免使用DOM相关的属性来用作其他的用途。
 - 代码对齐
```
<Foo
  superLongParam="bar"
  anotherSuperLongParam="baz"
>
  <Quux />
</Foo>
```
- 空格，总是在自动关闭的标签前加一个空格，正常情况下也不需要换行.
```
<Foo />
```
- Props 属性:JSX属性名使用骆驼式风格。
```
<Foo
  userName="hello"
  phoneNumber={12345678}
/>
```
 - Parentheses 括号:将多行的JSX标签写在 ()里. 
```
render() {
  return (
    <MyComponent className="long body" foo="bar">
      <MyChild />
    </MyComponent>
  );
}
//单行可以不需要
render() {
  const body = <div>hello</div>;
  return <MyComponent>{body}</MyComponent>;
}
```
 - 标签
    - 对于没有子元素的标签来说总是自己关闭标签. 
```
<Foo className="stuff" />
```
    - 如果模块有多行的属性， 关闭标签时新建一行.
```
<Foo
  bar="bar"
  baz="baz"
/>
```
