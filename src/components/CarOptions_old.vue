<template>
<div class="container">
    <h2>Car - Options API</h2>
    <p>Marca: {{brand}}</p>
    <p>Modelo: {{model}}</p>
    <p>Año: {{year}}</p>
    <p>Power: {{power}} HP</p>
    <button type="button" @click="increasePower(10)">Aumentar</button>
    <button type="button" @click="decreasePower(10)">Disminuir</button>
</div>
</template>

<script>
export default {
   data() {
         return {
              brand: "paganni",
              model: "huayra",
              year: "2020",
              power: "200"
         };
    },
    methods: {
        increasePower(newPower) {
            console.log('increasePower' + this.power);
            this.power =  newPower + this.power++;
            /* this.power++; */
          
        },
        decreasePower(newPower) {
            console.log('decreasePower' + this.power);
            this.power = this.power - newPower--;
            /* this.power--; */
        }
    }
   

};
</script>

<style>

</style>