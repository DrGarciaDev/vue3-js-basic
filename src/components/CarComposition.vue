<template>
    <div>
        <h2>Coche - Composition API</h2>
        <p>Marca {{ brand }}</p>
        <p>Model {{ model }}</p>
        <p>Potencia {{ power }}</p>

        <button @click="upPower(10)">Aumentar</button>
        <button @click="downPower">Disminuir</button>
    </div>
</template>

<script>
import { ref } from 'vue';

export default {
    // Esta es la forma de la API de composición o Composition API usada en VUE 3
    setup() {
        const brand = 'Audi';
        const model = "A4";
        let power = ref(60);

        const upPower = (newPower) => {
            console.log('Aumentando potencia ... ');
            // power.value ++;
            // console.log(power.value);
            power.value = power.value + newPower;
        };

        const downPower = () => {
            console.log('Disminuyendo potencia ... ');
            power.value --;
        };

        return {
            brand,
            model,
            power,
            upPower,
            downPower,
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