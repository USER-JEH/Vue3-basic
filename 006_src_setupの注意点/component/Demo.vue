<template>
<h1>App componet</h1>
<h2>name:{{person.name}}</h2>
<h2>age:{{person.age}}</h2>
<button @click="test">test</button>
</template>

<script>
// import {h} from 'vue'
import {reactive} from 'vue'
export default {
  name: 'Demo',
  props:['msg','school'],
  emits:['hello'],
  setup(props,context){
    // console.log('---setup---',props)
    console.log('---setup---',context)
    let person =reactive({
      name:'amy',
      age: 10
    })

    function test(){
      context.emit('hello',666)
    }
    return{
     person,
     test
    }

    // return()=> h('h','shangguigu')
  }
}
</script>

