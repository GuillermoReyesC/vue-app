<template>
<div class="container">
    <h2>Car - composition API</h2>
    <p>brand: {{brand}}</p>
    <p>Model: {{model}}</p>
    <p>year: {{year}}</p>
    <p>power: {{power}}</p>
    <button @click="upPower">Aumentar potencia </button>
    <button @click="downPower">Disminuir potencia</button>

   
</div>
</template>

<script>

export default {

    props: {
        power:{
            type: Number,
            default: '60',
        },
        upPower: Function,
        downPower: Function,
    },

    emits: ["downPower"],


setup(props, context) {

        const brand = "Ford";
        const model = "Mustang";
        const year = "2015";

        console.log(context);

        const downPowerFn = () => {
            context.emit("downPower");
        }

        console.log(props);
  //      console.log(props.power);
              
        return {
            brand,
            model,
            year,

        };

    },

};
</script>

<style>

</style>