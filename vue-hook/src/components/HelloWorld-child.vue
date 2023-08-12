<script setup>
import {onBeforeUnmount, onUnmounted} from "vue";


// #5 before unmounted
onBeforeUnmount(()=> {
    console.log('(hellow child) before unmounted onBeforeUnmount()')
})

// #6 when unmounted
onUnmounted(()=> {
    console.log('(hellow child) when unmounted onUnmounted()')
})

</script>

<template>
    <div>
        <h2>this is hellow child</h2>
    </div>

</template>

<style scoped>

</style>
