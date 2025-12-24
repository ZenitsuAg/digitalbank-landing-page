<script setup>
const props = defineProps(['img', 'alt', 'by', 'title', 'details'])
</script>

<template>
    <div class="rounded-[5px] overflow-hidden bg-white">
        <img :src="img" :alt="alt">

        <div class="py-300  flex items-center justify-center">
            <div class="w-66.25">
                <p class="text-preset-8 text-gray-600 mb-200">By {{ by }}</p>

                <h1 class="text-preset-6 mb-100 text-Blue">{{ title }}</h1>

                <p class="text-preset-7 text-gray-600">{{ details }}</p>
            </div>
        </div>
    </div>
</template>