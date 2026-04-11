<script setup lang="ts">
defineProps({
  title: String,
})
</script>

<template>
  <h3 class="text-xl lg:text-2xl font-semibold text-gray-700 dark:text-slate-200 mt-6 mb-4">{{ title }}</h3>
</template>
