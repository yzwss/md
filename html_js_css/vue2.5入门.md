

## Vue�����﷨
### ������һ��Vueʵ��
el:"#id"
template:
data:{}
{{msg}}��ֵ���ʽ

### ���ص㡢ģ���ʵ��
Vueֻ�ᴦ����ص����������
���ص������������ģ��
template:'<h1></h1>'

### Vueʵ���е����ݡ��¼��ͷ���
v-text="data�еı�����"
v-html="data�еı�����"
v-on:click="methods�еķ�����"
����DOM��Ϊ�������ݱ��
@click
data�еı�������methods/computed�еķ�����������ֱ��this.xxx���õ�

### Vue�е����԰󶨺�˫�����ݰ�
v-bind:title="data�еı�����(ֻҪ����vueģ��ָ��Ⱥź���ʵ����һ��js�ı��ʽ������һ��js���)"
:title
v-model="data�еı�����"

### Vue�еļ������Ժ�������
computed:{fullname:function(){return firstname + lastname}}
watch:{firstName(data�еı�������computed�еķ�����):function(){do something}}

### ������ѭ��
v-if="data�еı�����flag�����ʽ��"��ֱ��ɾ��DOM
v-show="data�еı�����flag�����ʽ��"��css����DOM
v-for="(item, index) of data�еı�����list" :key="item����index" :content(������)="item" :index="index" @delete=""     {{item}}

## Vue�е����
һ��html��ǩ��Ӧһ��data�еı�����Ȼ�����¼���������ϵ��Щ����
Vue.component('todo-item',{})ȫ�����
var TodoItem={
template:
props:['content', 'index']      �������Ǵ������ﴫ����
}�ֲ����
components:{'todo-item':{}}
�����ѭ����һ�£���ʵ�Ͳ����ö�������ˣ�����ÿ�������ֻ������һ���ⲿ����
this.$emit('delete', this.index)

## Vue-cli��ʹ��
npm install -g cnpm --registry=https://registry.npm.taobao.org������һ��
cnpm install -g vue-cli
vue init webpack todolist
cnpm run dev
cnpm run build
cnpm i element-ui -S
cnpm i v-charts echarts -S

����·�ɣ�App��ֱ��import HelloWorld
��·�ɣ�App������index.js������index.js����HelloWorld





ǰ��˷��뿪�������ǻ���ͬһ������˿ڣ����ÿ��ǿ������⡣ǰ��˸��ܸ���Ŀ¼��
��ǰ����ǰ�����ȫ���룬��Ϊ��ʹǰ��ֻ��View��������һ�������С�����ǰ��˸��ж������̣����ŵ�ͬһ���˿������С�