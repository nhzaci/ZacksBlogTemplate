<template>
    <div class="w-screen px-10 md:px-64 py-5 space-y-5">
        <div class="flex bg-green-300 w-full p-10 shadow-xl space-x-10 items-stretch">

            <div class="block bg-yellow-200 shadow-lg p-5 w-64 text-right lg:w-1/3">
                <h1 class="text-blue-800 font-semibold text-4xl p-2 bg-yellow-400 text-right shadow-lg">About me</h1>
            </div>
            
            <div class="flex items-center p-5 bg-orange-300 shadow-lg lg:w-1/3 space-y-5 items-stretch">
                <div class="flex p-5 bg-orange-400 shadow-lg">
                    <span class="p-2 h-auto text-right space-y-5 text-xl text-blue-900">
                        <p class="font-semibold">
                            I am a Sophomore majoring in Business Analytics in University.
                        </p>
                        <p class="font-serif">
                            My interest lies in machine learning and I an looking to integrate
                            Natural Language Processing into my web applications.
                        </p>
                    </span>
                </div>
            </div>

            <div class="block p-5 bg-blue-500 shadow-lg text-xl text-center lg:w-1/3">
                <h1 class="text-2xl font-bold p-2 bg-blue-600 shadow-lg text-gray-200">My Skills:</h1>
                <ul class="mt-5 px-20">
                    <li v-for="skill in skills" :key="skill" class="font-semibold text-white p-1">
                        {{skill}}
                    </li>
                </ul>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            skills: ['Nuxt.js', 'Vue.js', 'Java', 'Python', 'Tableau' ,'Django', 'Tailwind CSS']
        }
    }
}
</script>

<style>
    
</style>