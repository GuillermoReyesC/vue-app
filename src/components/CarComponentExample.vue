<template>
 <div>
     <h2>simply car</h2>
    <p>Marca: {{brand}}</p>
    <p>Modelo: {{model}}</p>
    <p>Año: {{year}}</p>
    {{ message.text }} from: {{ message.author }}
<!--     <p>Color:
        <span v-for="(color, index) in colors" :key="index">
        {{index}}:
        {{color}}-
        </span>
    </p> -->
    <ul>
        <li v-for="(color, index) in colors" :key="index">
            {{index}}: {{color}}
        </li>
    </ul>
    <p>Precio: $ {{price}}</p>
   <!--  <p>Potencia: {{powers}} HP</p> -->

   <p>
        Potencias Urbanas menor a 300 cv
   </p>
   <ul>
      <!--   <li v-for="(power, index) in powers" :key="index">
        <template v-if="power < 300">
            {{power}}

        </template>
         
        </li> -->

        <template v-for="(power, index) in powers" :key="index">
            <li v-if="power < 270"> Velocidad Urbana: {{power}} </li>    <!-- v-for recorre la data de la base de datos o store de datos-->
            <li v-else-if="power == 280">Hibrido: {{power}} </li>       <!-- v-if realiza operaciones del if -->
            <li v-else>Velocidad Carretera: {{power}}</li>               <!-- v-else es un else al if anterior -->
            <li v-if="power == 500" >maxima velocidad: {{power}}</li> 
          
        </template>

   </ul>

<!--    <p>potencias urbanas mayor a 300 cv</p>
   <ul>
        <template v-for="(power, index) in powers" :key="index">
            <li v-if="power > 300">
                {{power}}
            </li>
        </template>


   </ul> -->

 </div>
</template>


<script>
export default {  /* asi obtengo la data directo de donde la declaro */
/*     data() {
        return {
            brand: 'Audi',
            model: 'A4',
            color: ['black', 'white', 'red'],
            year: '2018',
            price: '20000',
            power: '200',
            message: {
                author: 'me',                
                title: 'Hello World',
                text: 'This is a message',


                },
        };
    }, */
    /* aqui  hacemos lo mismo pero desde el api de opciones declarando y trbajando dentro del setup y devolviendo en el return */
    setup () {
        const brand = 'Audi';
        const model = 'A4';
        const colors = ['black', 'white', 'red', 'blue'];
        const price = '20000';
        const year = '2018';
        const powers = ['60','80','100','120','140','180','240','260','280','290','300','390','450','500'];
        const message = {
            title: 'Hello World inside the setup',
            text: 'This is a message',
            author: 'me',
        };

        return {
            brand,
            model,
            colors,
            year,
            price,
            powers,
            message,
        };


    },

};
</script>

<style>

</style>