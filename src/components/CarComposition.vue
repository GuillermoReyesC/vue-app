<template>
<div class="container">
    <h2>Car - composition API</h2>
    <p>Marca: {{brand}}</p>
    <p>Modelo: {{model}}</p>
    <p>Año: {{year}}</p>
    <p>Power: {{power}} HP</p>
    <button type="button" @click="increasePower(20)">Aumentar</button>
    <button type="button" @click="decreasePower(20)">Disminuir</button>
</div>
</template>

<script>

import  { ref } from 'vue';

export default {
    setup() {

        const brand = "Ford";
        const model = "Mustang";
        const year = "2020";
        let power = ref(200);

        const increasePower = (newPower) => {
           /*  power++; */
            /* power.value++; */
            power.value = power.value + newPower;
            console.log('increasePower' + power.value);
            
        };

        const decreasePower = (newPower) => {
            /* power--; */
           /*  power.value--; */
            power.value = power.value - newPower--;
            console.log('decreasePower'+ power.value );
        };

        
        return {
            brand,
            model,
            year,
            power,
            increasePower,
            decreasePower
        };

    },

};
</script>

<style>

</style>