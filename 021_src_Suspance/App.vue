<template>
  <div class="app">
    <h3>I am App components</h3>
      <Suspanse>
        <template v-slot:defalut>
          <Child/>
        </template>
        <template v-slot:fallback>
          <h1>loading</h1>
        </template>
      </Suspanse>
  </div>
</template>

<script>
// import Child from './components/Child'
import {defineAsyncComponent} from 'vue'
const Child =defineAsyncComponent(()=>import('./components/Child'))
export default {
  name:'App',
  components:{Child}
}
</script>

<style>
.app{
  background-color: gray;
  padding: 10px;
}
</style>