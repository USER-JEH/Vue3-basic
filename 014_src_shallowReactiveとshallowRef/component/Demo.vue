<template>
<h4>x:{{x.y}}</h4>
<button @click="x.y++">click add 1</button>
<hr>
<h2>name:{{name}}</h2>
<h2>age:{{age}}</h2>
<h2>salary:{{job.j1.salary}}</h2>
<button @click="name+='!'">change name</button>
<button @click="age++">add</button>
<button @click="job.j1.salary++">add</button>
</template>

<script>
// import {h} from 'vue'
import {ref,reactive,toRef,toRefs,shallowReactive,shallowRef} from 'vue'
export default {
  name: 'Demo',
  setup(){
    // let person = shallowReactive({
    let person = reactive({
        name:'zhangsan',
        age:18,
        job:{
          j1:{
            salary:20
          }
        }
      })
      let x = shallowRef({
        y:0
      })
    
    return{
      x,
      person,
      ...toRefs(person)
    }
  }
}

</script>

