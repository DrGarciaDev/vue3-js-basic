<template>
    <div>
        <h2>Coche - Composition API</h2>
        <p>Marca {{ brand }}</p>
        <p>Model {{ model }}</p>
        <p>Potencia {{ power }}</p>
        <button @click="upPower">Aumentar potencia</button>
        <button @click="downPowerFn">Disminuir potencia</button>
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
    emits: ['downPower'],
    setup(props, context) {
        const brand = 'Audi';
        const model = "A4";

        // console.log(props);
        // console.log(context);
        // de esta manera se pueden recibir y utilizar funciones recibidas con el 
        // custom event emit 
        const downPowerFn = () => {
            context.emit('downPower')
        };

        return {
            brand,
            model,
            downPowerFn,
        };
    },
};
</script>

<style>

</style>