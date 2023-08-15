<script setup>
import HelloWorld from './components/HelloWorld.vue'
import {onBeforeMount, onBeforeUpdate, onMounted, onUpdated, ref} from "vue";

const count_parent = ref(0);

// #1 before create DOM TREE initiated
onBeforeMount(()=> {
    console.log('this is parent onBeforeMount()')
})

// #2 after create DOM tree initiated
onMounted(()=> {
    console.log('this is parent')
});

// #3 Before DOM TREE Change
onBeforeUpdate(()=> {
    console.log('this is parent onBeforeUpdate()')
})

// #4 when DOM tree change
onUpdated(()=> {
    console.log(document.getElementById('count_parent').textContent)
})

// #5 before unmounted

// #6 when unmounted

</script>

<template>
    <div>
        <h2>this is parent</h2>
        <button id="count_parent" @click="count_parent++">{{ count_parent }}</button>
    </div>

  <HelloWorld  />
</template>

<style scoped>

</style>
