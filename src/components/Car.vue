<template>
    <div>
        <h2>Coche - Composition API</h2>
        <p>Marca {{ brand }}</p>
        <p>Model {{ model }}</p>
        <p>Potencia {{ power }}</p>
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
    },
    setup(props) {
        const brand = 'Audi';
        const model = "A4";

        console.log(props.power);

        return {
            brand,
            model,
        };
    },
};
</script>

<style>

</style>