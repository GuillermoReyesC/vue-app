<template>
 <div>
   <h1>
    a simple example of a component in vue.js
  </h1>
  <CarOptions/>
  <hr/>
  <CarComposition/>
 </div>
</template>

<script>
import CarComposition from './components/CarComposition.vue'
import CarOptions from './components/CarOptions.vue'
export default {
  components: {
    CarComposition,
    CarOptions
  }

}
</script>

<style>

</style>