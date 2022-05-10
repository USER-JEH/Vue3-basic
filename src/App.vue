<template>
<h1>App componet</h1>
<h2>name:{{person.name}}</h2>
<h2>age:{{person.age}}</h2>
<h2>job type:{{person.job.type}}</h2>
<h2>money:{{person.job.salary}}</h2>
<h2>hobby:{{person.hobby}}</h2>
<h2>{{person.job.a.b.c}}</h2>
<button @click="changeInfo">change infomation</button>
</template>

<script>
// import {h} from 'vue'
import {reactive} from 'vue'
export default {
  name: 'App',
  setup(){
    let person =reactive({
      name:'amy',
      age: 10,
      job:{
          type:'front',
        salary:'500000',
        a:{
          b:{
            c:666
          }
        }
      },
      hobby: ['read','drink','game']
    })

    function changeInfo(){
      person.name = 'bee'
      person.age = 55
      person.job.type = 'UI'
      person.job.salary = '300000'
      person.job.a.b.c = 999
      person.hobby[0] = 'cook'
    }

    return{
     person,
     changeInfo
    }

    // return()=> h('h','shangguigu')
  }
}
</script>

