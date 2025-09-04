<script setup lang="ts">
import { Badge } from '@/components/ui/badge'
import skills from '@/model/skills'

</script>

<template>
  <div class="flex flex-wrap gap-3">
    <div v-for="skill in skills" v-bind:key="skill.id">
      <Badge class="text-sm lg:text-md">{{ skill.name }}</Badge>
    </div>
  </div>
</template>
