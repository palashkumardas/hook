<script setup>
import { ref,onBeforeMount,onMounted } from 'vue';
const status =ref([]);

onBeforeMount(()=>{
status.value.push('onBeforeMount');
});

onMounted(()=>{
  status.value.push('onMounted');
})
</script>

<template>
  <section class="mx-auto container">
    <h1 class="my-5">Lifecycle Hooks</h1>
    <div class="flex justify-between mt-20">
      <div class="w-1/2">
        <img src="//vuejs.org/assets/lifecycle.16e4c08e.png" alt="">
      </div>
      <div class="text-2xl w-1/2">
        {{ status }}
      </div>
    </div>

  </section>

</template>

<style scoped>

</style>
