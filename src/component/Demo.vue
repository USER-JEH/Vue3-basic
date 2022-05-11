<template>
 <h2>add:{{sum}}</h2>
 <button @click="sum++">click me add 1</button>
<h2>now imfo:{{msg}}</h2>
<button @click="msg+='!'">change info</button>
</template>

<script>
// import {h} from 'vue'
import {ref,watch} from 'vue'
export default {
  name: 'Demo',
  setup(){
    let sum =ref(0)
    let msg = ref('hello')
    // case one
    // watch(sum,(newValue,oldValue)=>{
    //   console.log('sum changed',newValue,oldValue)
    // })

    watch([sum,msg],(newValue,oldValue)=>{
      console.log('sum or msg changed',newValue,oldValue)},
      {immediate : true }
    )
    return{
     sum,
     msg
    }
  }
}

</script>

