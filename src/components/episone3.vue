<script setup>
import { ref,onUpdated } from 'vue';
const message = ref('Hello World');

onUpdated(()=>{
  console.log("onUpdated");
})
function messageUpdate(){
  message.value="Hello Vue";
}
</script>

<template>
  <section class="mx-auto container">
    <h1 class="my-5">Lifecycle Hooks</h1>
    <div class="flex justify-between mt-20">
      <div class="w-1/2">
        <img src="//vuejs.org/assets/lifecycle.16e4c08e.png" alt="">
      </div>
      <div class="text-2xl w-1/2">
        {{ message }}
        <button @click="messageUpdate()">Update</button>
      </div>
      </div>
  </section>

</template>

<style scoped>

</style>
