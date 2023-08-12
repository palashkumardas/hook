<script setup>
import { ref,onBeforeMount } from 'vue';
const apiResponse=ref([]);
onBeforeMount(()=>{
  fetch('https://jsonplaceholder.typicode.com/posts/1')
  .then(response=>response.json())
  .then(data=>apiResponse.value=data);
});


</script>

<template>
  <section class="mx-auto container">
    <h1 class="my-5">Lifecycle Hooks</h1>
    <div class="flex justify-between mt-20">
      <div class="w-1/2">
        <img src="//vuejs.org/assets/lifecycle.16e4c08e.png" alt="">
      </div>
      <div class="text-2xl w-1/2">
        {{ apiResponse }}</div>
      </div>

  </section>

</template>

<style scoped>

</style>
