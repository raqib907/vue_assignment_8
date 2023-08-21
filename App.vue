<script setup>
import ChildComponent from "./components/ChildComponent.vue";
import { ref } from 'vue';

const parentMessage = ref("Hello from parent!");
const childMessage = ref("");

const handleChildEvent = (message) => {
  childMessage.value = message;
};
</script>
<template>
  <div class="bg-gray-200 min-h-screen flex items-center justify-center">
    <ChildComponent :message="parentMessage" @child-event="handleChildEvent" />
    <div class="mt-4 text-center">
      <p class="text-xl">Message from child: {{ childMessage }}</p>
    </div>
  </div>
</template>



<style scoped>

</style>
