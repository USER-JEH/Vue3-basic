<template>
<h1>App componet</h1>
<h2>name:{{name}}</h2>
<h2>age:{{age}}</h2>
<h2>job type:{{job.type}}</h2>
<h2>money:{{job.salary}}</h2>
<button @click="changeInfo">change infomation</button>
</template>

<script>
// import {h} from 'vue'
import {ref} from 'vue'
export default {
  name: 'App',
  setup(){
    let name = ref('amy')
    let age = ref(10)
    let job = ref({
        type:'front',
        salary:'500000'
    })

    function changeInfo(){
      name.value = 'bee'
      age.value = 55
      job.value.type = 'UI'
      job.value.salary = '300000'
    }

    return{
      name,
      age,
      changeInfo,
      job
    }

    // return()=> h('h','shangguigu')
  }
}
</script>

