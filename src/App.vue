<template>
 <div>
   <h1>
    a simple component in vue.js
  </h1>
  <Car :power="power"/>
  
  
 </div>
</template>

<script>
import Car from './components/Car.vue'

export default {
  components: {
    Car
  },

  setup() {

    let power = 30;

    return {
      power,
     
    }
  }

}
</script>

<style>

</style>