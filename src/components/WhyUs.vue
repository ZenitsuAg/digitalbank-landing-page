<script setup>
const props = defineProps(['imgSrc', 'imgAlt', 'title', 'content'])
</script>

<template>
    <div>
        <div class="flex justify-center">
            <img :src="imgSrc" :alt="imgAlt">
        </div>
        <div class="">
            <h1 class="text-preset-4 mb-6 mt-10">{{ title }}</h1>
            <p class="text-preset-7 text-gray-600">{{ content }}</p>
        </div>
    </div>

</template>