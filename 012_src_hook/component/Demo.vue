<template>
 <h2>add:{{sum}}</h2>
 <button @click="sum++">click me add 1</button>
 <hr>
 <h1>mouse:x:{{point.x}}   y:{{point.y}}</h1>
 <hr>
</template>

<script>
import {ref} from 'vue'
import usePoint from '../hooks/usePoint'
export default {
  name: 'Demo',
  setup(){
    let sum =ref(0)
    let point = usePoint()

    return{
     sum,point
    }
  },
}

</script>

