<template>
    <div class="flex-col shadow-md p-5 bg-blue-700 text-gray-400">
        <div class="shadow-md px-2 py-1 bg-blue-600">
           <h1 class="font-semibold text-2xl text-white">{{ capFirstWord(title) }}</h1>
        </div>
        <p class="p-5 text-xl font-serif">{{ capFirstWord(text) }}</p>
    </div>
</template>

<script>
export default {
    methods: {
        capFirstWord(text) {
            var textArr = String(text).split(' ')
            textArr[0] = textArr[0].toUpperCase()
            return textArr.join(" ")
        }
    },
    props: [
        'title',
        'text'
    ]
}
</script>

<style scoped>
</style>