<script setup>
defineProps({
    title: {
        type: String,
        default: 'Latest Recipes'
    },
    description: {
        type: String,
        default: 'If you are ready to change the way you design websites, then you\'ll want to use our block builder to make it fun and easy!'
    }
})
</script>
<template>
<div class="xl:w-1/2 w-11/12">
            <h1 role="heading" tabindex="0" class="text-6xl font-bold 2xl:leading-10 leading-0 text-center text-gray-800">Touching hundreds of lives</h1>
            <h2 role="contentinfo" tabindex="0" class="text-base leading-normal text-center text-gray-600 mt-5">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text Lorem Ipsum is simply dummy text of the printing</h2>
        </div>
</template>