<template>
    <div>
        <Car :power="power" :upPower="upPower" />
    </div>
</template>

<script>
import Car from './components/Car';
import { ref } from 'vue';

export default {
    components: {
        Car,
    },
    setup() {
        let power = ref(38);

        const upPower = () => {
            console.log('Aumentar power ...');
            power.value ++;
        }

        return {
            power,
            upPower,
        };
    },
}
</script>

<style>

</style>