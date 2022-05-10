<template>
<h1>App componet</h1>
<h2>name:{{name}}</h2>
<h2>age:{{age}}</h2>
<button @click="sayHello">speak</button>
</template>

<script>
// import {h} from 'vue'
export default {
  name: 'App',
  setup(){
    let name = 'amy'
    let age = 10

    function sayHello(){
      alert(`I am${name},I am${age}years old,Nice to meet you`)
    }

    return{
      name,
      age,
      sayHello
    }

    // return()=> h('h','shangguigu')
  }
}
</script>

