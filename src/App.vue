<template>
 <div>
   <h1>
    a simple component in vue.js
  </h1>
  <Car :power="power" :upPower="upPower" :downPower="downPower"/>
  
  
 </div>
</template>

<script>
import Car from './components/Car.vue'
import { ref } from 'vue';

export default {
  components: {
    Car
  },

  setup() {

    let power = ref(30);

    const upPower = () => {
      power.value++;
      console.log("increase power...");
    }

    const downPower = () => {
      power.value--;
      console.log("decrease power...");
    }

    return {
      power,
      upPower,
      downPower,
     
    }
  }

}
</script>

<style>

</style>