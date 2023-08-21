<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
  message: String,
});

const { emit } = defineEmits();

const sendMessageToParent = () => {
  emit('child-event', 'Hello from child!');
};
</script>
<template>
  <div class="bg-white p-4 rounded shadow">
    <p class="text-lg">{{ message }}</p>
    <button @click="sendMessageToParent" class="mt-2 bg-blue-500 hover:bg-blue-600 text-white px-3 py-2 rounded">
      Send Message to Parent
    </button>
  </div>
</template>



<style scoped>

</style>
