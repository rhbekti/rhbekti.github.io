<script setup lang="ts">
import workExpriences from '@/model/works'
import WorkItem from '@/components/work/WorkItem.vue'
import { Check, Circle, Dot } from 'lucide-vue-next'
import { Button } from '@/components/ui/button'
import { Stepper, StepperDescription, StepperItem, StepperSeparator, StepperTitle, StepperTrigger } from '@/components/ui/stepper'

const steps = [
  {
    step: 1,
    title: 'Software Engineer (FULLTIME)',
    description:
      'Dec 2024 - Present',
  },
  {
    step: 2,
    title: 'Full Stack Developer (INTERN)',
    description: 'Feb 2024 - Jun 2024',
  },
  {
    step: 3,
    title: 'Android Dev Program (SIB)',
    description:
      'Aug 2023 - Dec 2023',
  },
  {
    step: 4,
    title: 'Full Stack Developer (INTERN)',
    description:
      'Nov 2022 - Agu 2023',
  },
  {
    step: 5,
    title: 'IT Program (FULLTIME)',
    description:
      'May 2021 - Feb 2023',
  },
]
</script>

<template>
  <Stepper orientation="vertical" class="my-6 flex w-full max-w-md flex-col justify-start gap-10">
    <StepperItem v-for="step in steps" :key="step.step" v-slot="{ state }"
      class="relative flex w-full items-start gap-6" :step="step.step">
      <StepperSeparator v-if="step.step !== steps[steps.length - 1]?.step"
        class="absolute left-[18px] top-[38px] block h-[105%] w-0.5 shrink-0 rounded-full bg-muted group-data-[state=completed]:bg-primary" />
      <StepperTrigger as-child>
        <Button :variant="state === 'completed' || state === 'active' ? 'default' : 'outline'" size="icon"
          class="z-10 rounded-full shrink-0"
          :class="[state === 'active' && 'ring-2 ring-ring ring-offset-2 ring-offset-background']">
          <Check v-if="state === 'completed'" class="size-5" />
          <Circle v-if="state === 'active'" />
          <Dot v-if="state === 'inactive'" />
        </Button>
      </StepperTrigger>
      <div class="flex flex-col gap-1">
        <StepperTitle :class="[state === 'active' && 'text-primary']"
          class="text-sm font-semibold transition lg:text-base">
          {{ step.title }}
        </StepperTitle>
        <StepperDescription :class="[state === 'active' && 'text-primary']"
          class="text-xs text-muted-foreground transition md:not-sr-only lg:text-sm">
          {{ step.description }}
        </StepperDescription>
      </div>
    </StepperItem>
  </Stepper>
</template>
