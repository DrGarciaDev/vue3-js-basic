<template>
    <div>
        <h1>Nuestro primer componente</h1>
        <h2>Coche</h2>
        <p>Marca {{ brand }}</p>
        <p>Model {{ model }}</p>
        <p>Potencias</p>
        <ul>
            <!-- <li v-for="(power, index) in powers" :key="index">
                <template v-if="power < 300">
                    {{ power }}
                </template>
            </li> -->
            <template v-for="(power, index) in powers" :key="index">
                <li v-if="power < 280">Urbanas: {{ power }}</li>
                <li v-else-if="power === 280">Híbrido: {{ power }}</li>
                <li v-if="power > 300">Carreras: {{ power }}</li>
            </template>
        </ul>
        <!-- <p>Colors
            <span v-for="(color, index) in colors" :key="index">
                - {{ index }}: {{ color }}
            </span>
        </p>
        <ul>
            <li v-for="(color, index) in colors" :key="index">
                {{ index }}: {{ color }}
            </li>
        </ul>
        <p>Color 1 {{ colors[0] }}</p>
        <p>Price {{ price }}</p>
        <p>Power {{ power }}</p>
        <p>Mensaje como objeto <b>{{ mensaje }}</b></p>
        <p>Mensaje accediendo a las propiedades del objeto <b>{{ mensaje.title }}</b></p> -->
    </div>
</template>

<script>
export default {
    // Esta es la forma de la API de composición o Composition API usada en VUE 3
    setup() {
        const brand = 'Audi';
        const model = "A4";
        const powers = [60, 80, 120, 160, 200, 280, 300, 390, 540, 500];
        // const colors = ["Azul", 'Rojo', 'Verde'];
        // const price = 38000;
        // const power = 180;
        // const mensaje = {
        //     title: 'Hola mundo',
        //     text: 'Adiós',
        // };

        return {
            brand,
            model,
            powers,
            // colors,
            // price,
            // power,
            // mensaje
        };
    },
    // // Esta es la forma de la API de opciones u Options API, usada en VUE 2
    // data() {
    //     return {
    //         brand: "Audi",
    //         model: "A4",
    //         color: ["Azul", 'Rojo', 'Verde'],
    //         price: 38000,
    //         power: 180,
    //         mensaje: {
    //             title: 'Hola mundo',
    //             text: 'Adiós',
    //         }
    //     };
    // },
};
</script>

<style>

</style>