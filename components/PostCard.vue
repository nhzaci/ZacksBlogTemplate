<template>
    <div class="shadow-md p-5 bg-blue-700 text-gray-400">
       <h1 class="font-semibold text-2xl text-white">{{ title }}</h1>
       <p class="p-5 text-xl font-serif">{{ text }}</p>
    </div>
</template>

<script>
export default {
    props: [
        'title',
        'text'
    ]
}
</script>

<style scoped>
</style>