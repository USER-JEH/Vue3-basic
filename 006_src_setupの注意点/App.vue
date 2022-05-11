<template>
  <Demo @hello="showHelloMsg" msg="hello" school="fudandaxue">
    <template v-slot:pwe>
      <span>shangguigu</span>
    </template>
  </Demo>
</template>

<script>
// import {h} from 'vue'
import Demo from './component/Demo'
export default {
  name: 'App',
  components:{Demo},
  setup(){
    function showHelloMsg(value){
      alert(`you have hello event ok?:${value}`)
    }
    return{
      showHelloMsg
    }
  }
}
</script>

