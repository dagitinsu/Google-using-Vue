<script setup>
import { ref, defineEmits } from 'vue';

const isVisible = ref(true);

const toggleImageVisibility = () => {
  emit('buttonClicked');
};

defineEmits(['buttonClicked']);

 {
  isVisible,
  toggleImageVisibility
};
</script>

<template>
    
  <div class="flex justify-end space-x-3 pr-8 pt-6 snap-x text-sm items-center" >
    <div class="snap-center hover:underline">Gmail</div> 
    <div class="snap-center hover:underline">Images</div>
     <div class="snap-center">
      <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32"
       viewBox="0 0 24 24"><path fill="currentColor" 
       d="M8 8H4V4h4v4zm6-4h-4v4h4V4zm6 0h-4v4h4V4zM8 10H4v4h4v-4zm6 
       0h-4v4h4v-4zm6 0h-4v4h4v-4zM8 16H4v4h4v-4zm6 0h-4v4h4v-4zm6 0h-4v4h4v-4z"/>
      </svg>
    </div>
    <div class="snap-center">
      <button @click="toggleImageVisibility" class="bg-[#2E6DD3] text-white p-1">Sign up</button>
    </div>
  </div>
</template>


<style>

</style>