<template>
    <div class="w-screen bg-blue-700 relative shadow-lg">
        <img src="@/assets/images/mountain.jpeg" class="object-cover h-96 w-screen" style="-webkit-filter: brightness(50%); filter:brightness(40%);" alt="Cover Image">
        <div class="centered text-white text-5xl font-serif font-semibold">
            ZACK's BLOG
        </div>
        <div class="absolute bottom-0 flex justify-center bg-teal-300 w-full h-20 items-center">
            <div class="space-x-12">
                <nuxt-link type="button" to="/" class="text-xl text-blue-700 hover:text-orange-500">
                    HOME
                </nuxt-link>
                <nuxt-link type="button" to="/about" class="text-xl text-blue-700 hover:text-orange-500">
                    ABOUT
                </nuxt-link>
                <nuxt-link type="button" to="/contact" class="text-xl text-blue-700 hover:text-orange-500">
                    CONTACT
                </nuxt-link>
                <nuxt-link type="button" to="/" class="text-xl text-blue-700 hover:text-orange-500">
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
.container {
  position: relative;
}

/* Bottom right text */
.text-block {
  position: absolute;
  bottom: 20px;
  right: 20px;
  background-color: black;
  color: white;
  padding-left: 20px;
  padding-right: 20px;
}

.centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>