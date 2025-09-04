<script setup lang="ts">
import EducationItem from '@/components/education/EducationItem.vue';

const education = {
  logo: '/images/education/utdi-logo.png',
  educationName: 'UNIVERSITAS TEKNOLOGI DIGITAL INDONESIA',
  studyProgram: 'SISTEM INFORMASI',
  studyDuration: 'SEP 2021 - MEI 2025'
};

</script>

<template>
  <div>
    <EducationItem :logo="education.logo" :education-name="education.educationName"
      :study-program="education.studyProgram" :study-duration="education.studyDuration" />
  </div>
</template>
