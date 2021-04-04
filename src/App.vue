<template>
    <div>
        <Car :power="power" />
    </div>
</template>

<script>
import Car from './components/Car';

export default {
    components: {
        Car,
    },
    setup() {
        let power = 38;

        return {
            power,
        };
    },
}
</script>

<style>

</style>