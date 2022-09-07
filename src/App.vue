<template>

  <div v-cloak class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
    <!-- We've used 3xl here, but feel free to try other max-widths based on your needs -->
    <div class="flex h-screen mx-auto max-w-3xl items-center">
      
      <div class="flex-1 text-sm rounded-md shadow-md bg-white p-5">
        <h1 class="text-2xl font-bold">{{ name }}</h1>

        <hr class="my-10">

        <button type="button" @click="emitter.emit('show-notification', {'type': 'info', 'title': 'Some information', 'message': 'This is a test message'})" class="text-blue-500 border border-blue-500 hover:bg-blue-500 hover:text-white rounded-md px-5 py-2 mr-5">Info</button>
        <button type="button" @click="emitter.emit('show-notification', {'type': 'success', 'title': 'Some success', 'message': 'This is a test message'})" class="text-green-500 border border-green-500 hover:bg-green-500 hover:text-white rounded-md px-5 py-2 mr-5">Success</button>
        <button type="button" @click="emitter.emit('show-notification', {'type': 'error', 'title': 'Some errors occurred', 'message': 'This is a test message'})" class="text-red-500 border border-red-500 hover:bg-red-500 hover:text-white rounded-md px-5 py-2 mr-5">Error</button>
        <button type="button" @click="emitter.emit('show-notification', {'type': 'warning', 'title': 'Some warnings occurred', 'message': 'This is a test message'})" class="text-yellow-500 border border-yellow-500 hover:bg-yellow-500 hover:text-white rounded-md px-5 py-2 mr-5">Warning</button>

      </div>
    
    </div>
  </div>

  <notification></notification>

</template>
  
<script setup>
import { ref } from 'vue';
import Notification from './components/Notification.vue'

const name = ref('Brittain Wynyard');
</script>
