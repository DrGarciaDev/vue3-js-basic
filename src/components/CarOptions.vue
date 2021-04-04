<template>
    <div>
        <h2>Coche - Options API</h2>
        <p>Marca {{ brand }}</p>
        <p>Modelo {{ model }}</p>
        <p>Potencia {{ power }}</p>

        <button @click="upPower(50)">Aumentar</button>
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
            console.log('Aumentando potencia');
            this.power = this.power + newPower;
        },
        downPower() {
            console.log('Bajando potencia');
            this.power --;
        }
    }
};
</script>

<style>

</style>