<script setup>
const props = defineProps(['imgSrc', 'imgAlt', 'title', 'content'])
</script>

<template>
    <div class="flex-1">
        <div class="flex justify-center md:justify-start">
            <img :src="imgSrc" :alt="imgAlt">
        </div>
        <div class="">
            <h1 class="text-preset-4 mb-6 mt-10">{{ title }}</h1>
            <p class="text-preset-7 text-gray-600 md:text-base leading-6.5 tracking-[-0.25px]">{{ content }}</p>
        </div>
    </div>

</template>