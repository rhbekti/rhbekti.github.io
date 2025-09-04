<script setup lang="ts">
import { Header } from '@/components/header'
import { WorkList } from '@/components/work'
import SubTitle from '@/components/SubTitle.vue'
import { About } from '@/components/about'
import { Education } from '@/components/education'
import { Skill } from '@/components/skill'
</script>

<template>
  <main class="w-full lg:max-w-1/2 px-4 py-6 mx-auto">
    <Header />

    <SubTitle title="About" />
    <About />

    <SubTitle title="Work Experience" />
    <WorkList />

    <SubTitle title="Education" />
    <Education />

    <SubTitle title="Skills" />
    <Skill />
  </main>
</template>

<style scoped></style>
