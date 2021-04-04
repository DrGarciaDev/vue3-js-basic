<template>
    <div>
        <h2>Coche - Composition API</h2>
        <p>Marca {{ brand }}</p>
        <p>Model {{ model }}</p>
        <p>Potencia {{ power }}</p>

        <button @click="upPower">Aumentar</button>
        <button @click="downPower(300)">Disminuir</button>
    </div>
</template>

<script>
export default {
    // Esta es la forma de la API de composición o Composition API usada en VUE 3
    setup() {
        const brand = 'Audi';
        const model = "A4";
        const power = 60;

        const upPower = () => {
            console.log('Aumentando potencia ... ');
        };

        const downPower = (newPower) => {
            console.log('Disminuyendo potencia ... ' + newPower);
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