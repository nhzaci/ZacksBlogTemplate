<template>
    <div class="w-screen bg-blue-700 relative shadow-xl h-96">
        <img src="@/assets/images/mountain.jpeg" class="object-cover h-96 w-screen" style="-webkit-filter: brightness(50%); filter:brightness(40%);" alt="Cover Image">
        <div class="centered text-white text-3xl md:text-5xl font-serif font-semibold">
            ZACK's BLOG
        </div>
        <div class="absolute bottom-0 flex justify-center w-full h-20 items-center">
            <div class="space-x-12 text-lg md:text-xl">
                <nuxt-link type="button" to="/" class="text-gray-200 hover:text-orange-500">
                    HOME
                </nuxt-link>
                <nuxt-link type="button" to="/about" class="text-gray-200 hover:text-orange-500">
                    ABOUT
                </nuxt-link>
                <nuxt-link type="button" to="/contact" class="text-gray-200 hover:text-orange-500">
                    CONTACT
                </nuxt-link>
                <nuxt-link type="button" to="/" class="text-gray-200 hover:text-orange-500">
                    SOCIAL
                </nuxt-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
/* Container holding the image and the text */
.centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>