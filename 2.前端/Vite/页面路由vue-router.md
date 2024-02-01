# 页面路由vue-router

```js
<script>
import { createRouter, createWebHashHistory } from 'vue-router'
// 1. 定义路由组件.
// 也可以从其他文件导入
const Home = { template: '<div><p>----Home----</p></div>' }
const About = { template: '<div><p>----about----</p></div>' }

// 2. 定义一些路由
// 每个路由都需要映射到一个组件。
// 我们后面再讨论嵌套路由。
const routes = [
  { path: '/', component: Home },
  { path: '/about', component: About },
]

// 3. 创建路由实例并传递 `routes` 配置
// 你可以在这里输入更多的配置，但我们在这里
// 暂时保持简单
const router = createRouter({
  // 4. 内部提供了 history 模式的实现。为了简单起见，我们在这里使用 hash 模式。
  history: createWebHashHistory(),
  routes, // `routes: routes` 的缩写
})

export default router
</script>
```

note: 
import { createRouter, createWebHashHistory } from 'vue-router'


```html
<template>
<main>

</main>
<div id="app">
    <p>
        <!--使用 router-link 组件进行导航 -->
        <!--通过传递 `to` 来指定链接 -->
        <!--`<router-link>` 将呈现一个带有正确 `href` 属性的 `<a>` 标签-->
        <div>
          <router-link to="/">Go to Home</router-link>
        <router-link style = "margin-left:20px" to="/about">Go to About</router-link>
      </div>
      <hr />
      </p>
      <!-- 路由出口 -->
      <!-- 路由匹配到的组件将渲染在这里 -->
      <router-view></router-view>
    </div>
</template>
```

```js
import { createApp } from 'vue/dist/vue.esm-bundler'
import App from './App.vue'
import router from './components/rt.vue'

createApp(App).use(router).mount('#app')
```

note: router html should write in App and would be rendered