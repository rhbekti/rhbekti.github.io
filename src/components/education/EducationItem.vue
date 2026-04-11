<script setup lang="ts">
defineProps({
    logo: String,
    educationName: String,
    studyProgram: String,
    studyDuration: String,
})
</script>

<template>
    <div class="flex flex-row justify-between mb-4 items-center">
        <div class="flex items-center gap-4">
            <div
                class="rounded-xl xl:rounded-full overflow-hidden h-16 w-16 border border-gray-300 shadow-md p-3 dark:bg-white">
                <img :src="logo" alt="HLD Logo" class="w-full h-full object-cover" />
            </div>
            <div>
                <h4 class="text-gray-700 dark:text-slate-100 font-semibold">{{ educationName }}</h4>
                <h5 class="text-gray-500 font-mono dark:text-slate-200 text-sm font-medium">{{ studyProgram }}
                </h5>
            </div>
        </div>
        <div>
            <span class="text-gray-500 dark:text-slate-100">{{ studyDuration }}</span>
        </div>
    </div>
</template>
