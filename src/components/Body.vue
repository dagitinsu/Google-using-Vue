<script>
import { ref, watch } from 'vue';

const isVisible = ref(true);

watch(isVisible, (newValue) => {
  // Handle the image visibility directly inside the watch function
  const image = document.querySelector('img');

  if (newValue) {
    // Show the image
    image.style.display = 'block';
  } else {
    // Hide the image
    image.style.display = 'none';
  }
});

export default {
  props: {
    isVisible: Boolean,
  },
};
</script>

<template>
  
  <div class="flex justify-center pt-28">
    <img v-if="isVisible" src="/img/googlelogo.png" alt="google">
  </div>  
  <div class="flex justify-center items-center">
    <div class="flex mt-6 border-2 border-#D9D9D9 bg-[white] rounded-3xl w-2/5 h-12 items-center">
      <input type="text" class="ml-12 focus:outline-none ">      
  </div>
  </div>

  <div class="flex justify-center mt-7 space-x-3 font-arial text-13">
    <div>
      <button class="bg-[#FAF9F9] px-2 py-1 hover:border-2  hover:border-#D9D9D9 ">Google Search</button>
    </div>
    <div>
      <button class="bg-[#FAF9F9] px-2 py-1 hover:border-2  hover:border-#D9D9D9">I'm Feeling Lucky</button>
    </div>
  </div>
  <div class="flex justify-center mt-4">
    <div class="text-sm text-[#4d5156]">
      Google offered in: <span class="text-[#1a0dab]"> <a class="hover:underline"> አማርኛ </a> 
       <a class="hover:underline"> ትግርኛ</a> </span> 
    </div>
  </div>

</template>

<style>
</style>