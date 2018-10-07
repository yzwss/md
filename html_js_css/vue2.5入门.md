

## Vue基础语法
### 创建第一个Vue实例
el:"#id"
template:
data:{}
{{msg}}插值表达式

### 挂载点、模板和实例
Vue只会处理挂载点下面的内容
挂载点下面的内容是模板
template:'<h1></h1>'

### Vue实例中的数据、事件和方法
v-text="data中的变量名"
v-html="data中的变量名"
v-on:click="methods中的方法名"
面向DOM改为面向数据编程
@click
data中的变量名和methods/computed中的方法名都可以直接this.xxx引用到

### Vue中的属性绑定和双向数据绑定
v-bind:title="data中的变量名(只要用了vue模板指令，等号后面实际是一个js的表达式，就是一条js语句)"
:title
v-model="data中的变量名"

### Vue中的计算属性和侦听器
computed:{fullname:function(){return firstname + lastname}}
watch:{firstName(data中的变量名或computed中的方法名):function(){do something}}

### 条件与循环
v-if="data中的变量名flag（表达式）"，直接删除DOM
v-show="data中的变量名flag（表达式）"，css隐藏DOM
v-for="(item, index) of data中的变量名list" :key="item或者index" :content(参数名)="item" :index="index" @delete=""     {{item}}

## Vue中的组件
一个html标签对应一个data中的变量，然后用事件代码来联系这些变量
Vue.component('todo-item',{})全局组件
var TodoItem={
template:
props:['content', 'index']      函数就是从外往里传参数
}局部组件
components:{'todo-item':{}}
子组件循环了一下，其实就产生好多子组件了，但是每个子组件只接受了一个外部参数
this.$emit('delete', this.index)

## Vue-cli的使用
npm install -g cnpm --registry=https://registry.npm.taobao.org，多这一步
cnpm install -g vue-cli
vue init webpack todolist
cnpm run dev
cnpm run build
cnpm i element-ui -S
cnpm i v-charts echarts -S

不用路由：App里直接import HelloWorld
用路由：App里引入index.js，再由index.js引入HelloWorld





前后端分离开发，但是还是同一个服务端口，不用考虑跨域问题。前后端各管各的目录。
以前很难前后端完全分离，因为即使前端只管View，但还是一个工程中。现在前后端各有独立工程，最后放到同一个端口容器中。