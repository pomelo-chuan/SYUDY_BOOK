## FLOW

####flow 支持的原始数据类型：

1. boolean
2. number
3. string
4. null
5. void

其中**void**类型，即是js中的**undefined**类型

注意：

```javascript
null == undefined	// true

null === undefined	// false

```

string | number 表示两种类型中任何一种都可以使用，成为“联合（Union）类型”

最特别的是可选(Optional)类型的设计，可选代表这个变量的值可能不存在，也就是允许它除了是某个特定的值之外，也可以是**null**或者**undefined**。就是在类型名称定义前加上问好(?)，例如**?string**，以下是一个例子：

```javascript
let bar: ?string = null
```

#### 类型别名
类型别名（Type Alias）提供了可以预先定义与集中代码所需要的类型，一个简单的例子如下：

```javascript
type T = Array<string>
var x: T = []
x["Hi"] = 2	// 有flow警告
```

#### 任何的类型数据
any： 相当于不检查。即是所有类型的超集(supertype)，也是所有类型的子集(subtype)

mixed: 是一个特殊的类型