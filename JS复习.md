null 是没有值的数据类型，undedined是值缺少值的数据类型。

```js
alert( null > 0 );  // (1) false
alert( null == 0 ); // (2) false
alert( null >= 0 ); // (3) true
```

这是因为相等性检查 `==` 和普通比较符 `> < >= <=` 的代码逻辑是相互独立的。进行值的比较时，`null` 会被转化为数字，因此它被转化为了 `0`。这就是为什么（3）中 `null >= 0` 返回值是 true，（1）中 `null > 0` 返回值是 false。

```js
isNaN(1 + null)      // false
isNaN(1 + undefined) // true
alert( null == undefined ); // true
alert( 0 == NaN );//false
```

当使用数学式或其他比较方法 `< > <= >=` 时：

`null/undefined` 会被转化为数字：`null` 被转化为 `0`，`undefined` 被转化为 `NaN`。

模板字符串

```
var a = 1; console.log('一共有'+a+'个鸡蛋！')

那么现在你只要console.log(`一共有${a}个鸡蛋！`)
```

+ 引用类型==比较还要比较他的地址

+ this指向调用他的对象，如果在this指向的对象里添加一个子对象，那么这个子对象里的this指向子对象

  ```js
  obj1{
      this->obj1
  }
  obj1.obj2={
   this->obj2
  }
  call(传入this)
  使obj2的this指向改成obj1
  ```
