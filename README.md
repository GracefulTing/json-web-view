# json-web-view

> 一个展示通用json的vue组件，不需要关注数据结构，无论是数组还是对象，都可以按照格式化后的json结构显示在页面中。

``` bash
操作步骤：安装好该插件之后引入调用，然后传如对应的数组或者对象结构就可以了。
详细步骤：
1、安装该插件
npm install json-web-view;

2、使用
//引入
import jsonView from 'json-web-view'
//传json值
<jsonView :json="xxx"></jsonView>
```

``` bash
示例：App.vue
<template>
  <jsonView :json="data"></jsonView>
</template>

<script>
import jsonView from 'json-web-view'
components:{
  jsonView
},
data(){
  //数组
  data:[
    {
          label: '一级 1',
          children: [{
            label: '二级 1-1',
            children: [{
              label: '三级 1-1-1'
            }]
          }]
        }, {
          label: '一级 2',
          children: [{
            label: '二级 2-1',
            children: [{
              label: '三级 2-1-1'
            }]
          }, {
            label: '二级 2-2',
            children: [{
              label: '三级 2-2-1'
            }]
          }]
     },
     //对象
     //data:{
     //   "name":"a",
     //   "age":"18",
     //   "sex":"女"
     //}
  ]
}
</script>
```
