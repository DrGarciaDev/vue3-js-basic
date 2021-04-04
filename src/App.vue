<template>
    <div>
        <CarOptions />
        <hr>
        <CarComposition />
    </div>
</template>

<script>
import CarComposition from './components/CarComposition';
import CarOptions from './components/CarOptions';

export default {
    components: {
        CarComposition,
        CarOptions
    }
}
</script>

<style>

</style>