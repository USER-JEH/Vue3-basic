<template>
 <h2>add:{{sum}}</h2>
 <button @click="sum++">click me add 1</button>
<h2>now imfo:{{msg}}</h2>
<button @click="msg+='!'">change info</button>
<h2>name:{{person.name}}</h2>
<h2>age:{{person.age}}</h2>
<h2>salary:{{person.job.j1.salary}}</h2>
<button @click="person.name+='!'">change name</button>
<button @click="person.age++">add</button>
<button @click="person.job.j1.salary++">add</button>
</template>

<script>
// import {h} from 'vue'
import {ref,reactive,watch,watchEffect} from 'vue'
export default {
  name: 'Demo',
  setup(){
    let sum =ref(0)
    let msg = ref('hello')
    let person = reactive({
      name:'zhangsan',
      age:18,
      job:{
        j1:{
          salary:20
        }
      }
    })

    // watch(sum,(newValue,oldValue)=>{
    //   console.log(newValue,oldValue)
    // },{immediate:true})

    watchEffect(()=>{
      const x1 = person.job.j1.salary
      console.log('ok')
    })

    return{
     sum,
     msg,
     person
    }
  }
}

</script>

