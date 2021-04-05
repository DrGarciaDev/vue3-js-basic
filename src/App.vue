<template>
    <div>
        <!-- con : se mandan variables y/o funciones, con la @ se pueden mandar fucniones con el custom event emit -->
        <Car :power="power" :upPower="upPower" @downPower="downPower" />
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
            // console.log('Aumentar power ...');
            power.value ++;
        }

        const downPower = () => {
            // console.log('Disminuir power ...');
            power.value --;
        }

        return {
            power,
            upPower,
            downPower,
        };
    },
}
</script>

<style>

</style>