## CSS
```
1.自定义样式时  前缀用(wmui)  .wmui-XXX-XXX
2.使用less
```

## vue
```
1.vue组件中不能超过500行，（抽离css或封装components）
```

## vueRouter
#### 把组件按组分块
```
官网 https://router.vuejs.org/zh/guide/advanced/lazy-loading.html
有时候我们想把某个路由下的所有组件都打包在同个异步块 (chunk) 中。只需要使用 命名 chunk，一个特殊的注释语法来提供 chunk name (需要 Webpack > 2.4)。

const operPlatList = () => import(/* webpackChunkName: "operPlat" */ "@/pages/operPlat/list")
const operPlatDetail = () => import(/* webpackChunkName: "operPlat" */ "@/pages/operPlat/children/detail")

```

## eslint (项目中必须增加eslint)

```
  // "off" 或者 0：关闭规则。
  // "warn" 或者 1：打开规则，并且作为一个警告（不影响exit code）。
  // "error" 或者 2：打开规则，并且作为一个错误（exit code将会是1）。
  "rules": {
    "no-alert": 2, // 禁止使用alert confirm prompt
    "no-console": 2, // 禁止使用console
    "no-debugger": 2, // 禁止使用debugger
    "no-const-assign": 2, // 禁止修改const声明的变量
    "no-dupe-keys": 2, // 在创建对象字面量时不允许键重复 {a:1,a:1}
    "no-empty": 2, // 块语句中的内容不能为空
    "no-implicit-coercion": 2, // 禁止隐式转换
    "no-irregular-whitespace": 2, // 不能有不规则的空格
    "no-mixed-spaces-and-tabs": [2, false], // 禁止混用tab和空格
    "no-multiple-empty-lines": [2, { "max": 2 }], // 空行最多不能超过2行
    "curly": [2, "all"], //必须使用 if(){} 中的{}
    "semi-spacing": [2, { "before": false, "after": true }], // 分号前后空格
    "eqeqeq": 2, // 必须使用全等
  }
```

## 发版
```
发版前必须去掉alert、console、debugger
静态文件（css、js）必须带改时间戳，避免静态资源缓存
```

