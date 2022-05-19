<template>
  <input type="text" v-model="keyWord">
  <h3>{{keyWord}}</h3>
</template>

<script>
import {ref,customRef} from 'vue'
export default {
  name: 'App',
  setup(){
    function myRef(value){
      return customRef((track,trigger)=>{
        return{
          get(){
            track()
            return value
          },
          set(newValue){
            setTimeout(() => {
              value = newValue
              trigger()
            }, 1000);
          }
        }
      })
      
    }

    let keyWord =myRef('hello')
    return{keyWord}
  }
}

</script>

