<template>
<button @click="isShowDemo = !isShowDemo">on/off</button>
<hr>
<Demo v-if="isShowDemo"/>
<Test/>
</template>

<script>
import {ref} from 'vue'
import Demo from './component/Demo'
import Test from './component/Test'
export default {
  name: 'App',
  components:{Demo,Test},
  setup(){
    let isShowDemo =ref(true)
    return{isShowDemo}
  }
}

</script>

