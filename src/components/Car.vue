<template>
<div class="container">
    <h2>Car - composition API</h2>
    <p>Marca: {{brand}}</p>
    <p>Modelo: {{model}}</p>
    <p>Año: {{year}}</p>

   
</div>
</template>

<script>



export default {

    props: {
        power:{
            type: Number,
            default: '60'
        },
    },

setup(props) {

        const brand = "Ford";
        const model = "Mustang";

        console.log(props);

        
        return {
            brand,
            model,

        };

    },

};
</script>

<style>

</style>