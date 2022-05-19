<template>
  <div class="app">
    <h3>I am App components,{{name}},{{price}}</h3>
    <Child/>
  </div>
</template>

<script>
import { reactive,toRefs,provide } from 'vue'
import Child from './components/Child.vue'
export default {
  name:'App',
  components:{Child},
  setup(){
    let car = reactive({
      name:'benc',
      price:'40w'
    })
    provide('car',car)
    return {...toRefs(car)}
  }
}
</script>

<style>
.app{
  background-color: gray;
  padding: 10px;
}
</style>