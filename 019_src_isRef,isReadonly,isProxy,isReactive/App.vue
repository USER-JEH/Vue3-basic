<template>
  <h3>I am App components</h3>
</template>

<script>
import { ref,reactive,toRefs, readonly,isRef,isReadonly,isProxy,isReactive} from 'vue'
export default {
  name:'App',
  setup(){
    let car = reactive({
      name:'benc',
      price:'40w'
    })
    let sum = ref(0)
    let car2 = readonly(car)

    console.log(isRef(sum))
    console.log(isReactive(car))
    console.log(isReadonly(car2))
    console.log(isProxy(car))


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