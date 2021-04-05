<template>
    <div>
        <h2>Coche - Composition API</h2>
        <p>Marca {{ brand }}</p>
        <p>Model {{ model }}</p>
        <p>Potencia {{ power }}</p>
        <button @click="upPower">Aumentar potencia</button>
    </div>
</template>

<script>
export default {
    // Esta es la forma de la API de composición o Composition API usada en VUE 3
    props: {
        power: {
            type: Number,
            default: 60,
        },
        upPower: Function,
    },
    setup(props) {
        const brand = 'Audi';
        const model = "A4";

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