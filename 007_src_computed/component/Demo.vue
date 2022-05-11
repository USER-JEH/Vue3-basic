<template>
<h1>App componet</h1>
First name:<input type="text" v-model="person.firstName">
Last name: <input type="text" v-model="person.lastName">
<span>fullname:{{person.fullName}}</span> 
</template>

<script>
// import {h} from 'vue'
import {reactive,computed} from 'vue'
export default {
  name: 'Demo',
  setup(){
    let person =reactive({
      firstName:'zhang',
      lastName:'wu'
    })
    person.fullName = computed(()=>{
      return person.firstName + person.lastName
    })

    return{
     person
    }

    // return()=> h('h','shangguigu')
  }
}
</script>

