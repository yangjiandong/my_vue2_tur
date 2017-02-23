Vue2.0 官方教程
====

02.22
----

### google font local save

firefox addon (https://addons.mozilla.org/en-US/firefox/addon/decentraleyes/)

### keep-alive

所有的都缓存在内存中

### functional

意味它是无状态(没有 data),无实例(没有 this 上下文);只渲染视图而不能进行逻辑操作

### url query

```
<!-- 带查询参数，下面的结果为 /register?plan=private -->
<router-link :to="{ path: 'register', query: { plan: 'private' }}">Register</router-link>
```

### HTML5 history 模式

vue-router 默认 hash 模式 —— 使用 URL 的 hash 来模拟一个完整的 URL，于是当 URL 改变时，页面不会重新加载。

使用 history 模式时，URL 就像正常的 url，例如 `http://yoursite.com/user/id`，也好看！

### vue-router 路由懒加载

对应的组件定义成异步组件：

```
const Foo = resolve => {
  // require.ensure 是 Webpack 的特殊语法，用来设置 code-split point
  // （代码分块）
  require.ensure(['./Foo.vue'], () => {
    resolve(require('./Foo.vue'))
  })
}
```

or

使用 AMD 风格的 require

```
const Foo = resolve => require(['./Foo.vue'], resolve)
```

不需要改变任何路由配置，跟之前一样使用 Foo：

```
const router = new VueRouter({
  routes: [
    { path: '/foo', component: Foo }
  ]
})
```

02.21
----

- 教程学习结束
- vue-router, [vue-router gitbook](http://router.vuejs.org/zh-cn/)

2017.02.16
----

[Vue2.0 guide](https://cn.vuejs.org/v2/guide/)

组件
----

- 父组件通过 props 向下传递数据给子组件，子组件通过 events 给父组件发送消息。(props down, events up)

<img src="props-events.png">

sublime text3
----

- editorconfig
- prettify

  html,css,js format code(cmd+shift+h)
- scss,sass: Syntax Highlighting for Sass
- Color Hightlighter, show color for hex or rgb
- local history
- key

  Ctrl+Shift+M：选中花括号里面的全部内容不包括{}。


