<template>
    <div>
        <h2>Coche - Options API</h2>
        <p>Marca {{ brand }}</p>
        <p>Modelo {{ model }}</p>
        <p>Potencia {{ power }}</p>

        <button @click="upPower(1000)">Aumentar</button>
        <button @click="downPower">Disminuir</button>
    </div>
</template>

<script>
export default {
    // Esta es la forma de la API de opciones u Options API, usada en VUE 2
    data() {
        return {
            brand: "Seat",
            model: "Leon",
            power: 60,
        };
    },
    methods: {
        upPower(newPower) {
            console.log('Aumentando potencia -> ' + newPower);
        },
        downPower() {
            console.log('Bajando potencia');
        }
    }
};
</script>

<style>

</style>