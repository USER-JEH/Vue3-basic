<template>
<button @click="isShowDemo = !isShowDemo">on/off</button>
<hr>
<Demo v-if="isShowDemo"/>
</template>

<script>
import {ref} from 'vue'
import Demo from './component/Demo'
export default {
  name: 'App',
  components:{Demo},
  setup(){
    let isShowDemo =ref(true)
    return{isShowDemo}
  }
}

</script>

