<script setup lang="ts">
defineProps({
  logo: String,
  work: String,
  position: String,
  time: String,
})
</script>

<template>
  <div class="flex flex-row justify-between mb-4 items-center">
    <div class="flex items-center gap-4">
      <div
        class="rounded-xl xl:rounded-full overflow-hidden h-16 w-16 border border-gray-300 shadow-md p-3"
      >
        <img :src="logo" alt="HLD Logo" class="w-full h-full object-cover" />
      </div>
      <div>
        <h4 class="text-gray-700 text-sm lg:text-lg font-semibold">{{ work }}</h4>
        <h5 class="text-gray-500 font-sans text-sm lg:text-lg">{{ position }}</h5>
      </div>
    </div>
    <div>
      <span class="text-gray-500 text-sm lg:text-lg">{{ time }}</span>
    </div>
  </div>
</template>
