# TypeScript

## 泛型

```js
function identity <T>(value:T): T{
  return value;
}
```

上面这个函数中的T就是一个希望传给identity函数的类型占位符。

![ts-泛型](/Users/shizu/code/notes/images/ts-泛型.png)

其实T可以用任何字母代替。

常见的泛型类型有：

- T（Type）表示类型
- K（Key）表示对象中的键的类型
- V（Value）表示对象中值的类型
- E（Element）表示元素类型

```Js
function identity <T,U>(value: T,message: U) : T{
  console.log(message);
  return value;
}
// 显示指定泛型变量的实际类型
console.log(identity<number,string>(68,"number"));
// 不置顶泛型变量的实际类型
console.log(identity(68,"number"));
```
