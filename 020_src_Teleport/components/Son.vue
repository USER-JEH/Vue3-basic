<template>
  <div class="son">
    <h3>I am son components</h3>
    <Dialog/>
  </div>
</template>

<script>
import Dialog from './Dailog.vue'
export default {
  name:'Son',
  components:{Dialog}
  }
</script>

<style>
.son{
  background-color: orange;
  padding: 10px;
}
</style>