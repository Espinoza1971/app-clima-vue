<script setup>

import useClima from '../composobles/useClima';

const { formatearTemperatura } = useClima()

defineProps({
    clima: {
        type:Object,
        required: true
    }
})
</script>

<template>
    <div class="resultado">
        <h2>Clima de: {{clima.name}} </h2>
        <p class="actual">&deg;C {{ formatearTemperatura(clima.main.temp) }}</p>
        <div class="temperaturas">
            <p>Min: <span>&deg;C {{ formatearTemperatura(clima.main.temp_min) }}</span></p>
            <p>Máx: <span>&deg;C {{ formatearTemperatura(clima.main.temp_max) }}</span></p>
        </div>
    </div>
</template>


