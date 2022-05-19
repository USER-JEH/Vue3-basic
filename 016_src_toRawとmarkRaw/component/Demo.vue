<template>
<h4>sum is :{{sum}}</h4>
<button @click="sum++">click add 1</button>
<hr>
<h2>name:{{name}}</h2>
<h2>age:{{age}}</h2>
<h2>salary:{{job.j1.salary}}</h2>
<h2 v-show="person.car">car:{{person.car}}</h2>
<button @click="name+='!'">change name</button>
<button @click="age++">add</button>
<button @click="job.j1.salary++">add</button>
<button @click="showRowPerson">original person</button>
<button @click="addCar">add car</button>
<button @click="person.car.name+='!'">change car name</button>
<button @click="person.car.price++">change car number</button>
</template>

<script>
// import {h} from 'vue'
import {ref,reactive,toRefs,toRaw, markRaw} from 'vue'
export default {
  name: 'Demo',
  setup(){
    let sum = ref(0)
    let person = reactive({
        name:'zhangsan',
        age:18,
        job:{
          j1:{
            salary:20
          }
        }
      })
      
    function showRowPerson(){
      const p = toRaw(person)
      p.age++
      console.log(p)
    }

    function addCar(){
      let car = { name:'benc',price:40}
      person.car =markRaw( car )
    }

    return{
      sum,
      person,
      ...toRefs(person),
      showRowPerson,
      addCar
  }
}
}

</script>

