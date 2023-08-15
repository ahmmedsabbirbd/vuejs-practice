<script setup>
import {ref, onMounted, onUpdated, onBeforeUpdate} from "vue";
import HelloWorldChild from "./HelloWorld-child.vue";

const count_child = ref(0);
const show = ref(false)

// after create DOM tree
onMounted(()=> {
    console.log('this is child')
});

// when DOM tree change
onUpdated(()=> {
    console.log('updated hellow')
    console.log(document.getElementById('count_child').textContent)
})


</script>

<template>
    <div>
        <h2>this is child</h2>
    </div>

    <button id="count_child" @click="count_child++">{{ count_child }}</button>

    <br>
    <button @click="show=true">Show HelloWorldChild</button>
    <button @click="show=false">hide HelloWorldChild</button>

    <HelloWorldChild v-if="show"/>
</template>

<style scoped>

</style>
