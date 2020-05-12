<template>
    <div class="flex-col shadow-md p-5 bg-blue-700 text-gray-400">
        <div class="shadow-md px-2 py-1 bg-blue-600">
           <h1 class="font-semibold text-2xl text-white">{{ capFirstWord(title) }}</h1>
        </div>
        <div class="m-5 p-5 bg-yellow-300 shadow-lg">
            <img :src="fullImgUrl(imgurl)" alt="Image sposed to b here" class="h-32 object-cover w-full"/>
            <p class="p-5 text-xl font-serif text-blue-700">{{ capFirstWord(post) }}</p>
        </div>
        <p class="text-right">
            Tags: {{ tags }}
        </p>
        <p class="text-right">
            {{ formatDateTime(created) }}
        </p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            months: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec']
        }
    },
    methods: {
        capFirstWord(text) {
            var textArr = String(text).split(' ')
            textArr[0] = textArr[0].toUpperCase()
            return textArr.join(" ")
        },
        formatDateTime(obj) {
            obj = new Date(obj)
            var year = obj.getFullYear()
            var month = this.months[obj.getMonth()]
            return obj
        },
        fullImgUrl(url) {
            var images = require.context('../assets/images', false, /\.jpeg$/)
            return images('./' + url)
        }
    },
    props: [
        'title',
        'post', 
        'created',
        'tags',
        'imgurl'
    ]
}
</script>

<style scoped>
</style>