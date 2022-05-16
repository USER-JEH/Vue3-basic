<template>
    <h2>Test</h2>
     <h1>mouse:x:{{point.x}}   y:{{point.y}}</h1>
     <hr>
</template>

<script>
import usePoint  from '../hooks/usePoint'
export default{
    name:'Test',
    setup(){
      const point = usePoint()

      return {point}
    }
}
</script>