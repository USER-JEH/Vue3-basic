<template>
<h2>name:{{name}}</h2>
<h2>age:{{age}}</h2>
<h2>salary:{{job.j1.salary}}</h2>
<button @click="name+='!'">change name</button>
<button @click="age++">add</button>
<button @click="job.j1.salary++">add</button>
</template>

<script>
// import {h} from 'vue'
import {reactive,toRef,toRefs} from 'vue'
export default {
  name: 'Demo',
  setup(){
    let person = reactive({
      name:'zhangsan',
      age:18,
      job:{
        j1:{
          salary:20
        }
      }
    })

    const x = toRefs(person)
    console.log('ok',x)
    
    return{
      person,
      // name:toRef(person,'name'),
      // age:toRef(person,'age'),
      // salary:toRef(person.job.j1,'salary')

      ...toRefs(person)
    }
  }
}

</script>

