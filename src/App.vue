<script setup lang="ts">
import { Header } from '@/components/header'
import { WorkList } from '@/components/work'
import SubTitle from '@/components/SubTitle.vue'
import { About } from '@/components/about'
import { Education } from '@/components/education'
</script>

<template>
  <Header />

  <main class="relative mx-auto flex w-full max-w-5xl flex-1 flex-col pt-32">
    <About />

    <SubTitle title="Work Experience" />
    <WorkList />

    <SubTitle title="Education" />
    <Education />
  </main>
</template>

<style scoped></style>
