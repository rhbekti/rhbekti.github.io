<script setup lang="ts">
import workExpriences from '@/model/work'
import WorkItem from '@/components/work/WorkItem.vue'
</script>

<template>
  <div class="flex flex-col gap-4" v-for="work in workExpriences" :key="work.id">
    <WorkItem :logo="work.logo" :work="work.title" :position="work.position" :time="work.time" />
  </div>
</template>
