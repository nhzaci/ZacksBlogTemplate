<template>
  <div class="w-screen">

    <!-- Remainder of the page -->
    <div class="flex lg:mx-64 mx-5 mt-5">
      <!-- Left side of the page -->
      <div class="w-full lg:w-3/4 bg-green-300 space-y-5 p-5 shadow-lg">
        <PostCard v-for="post in posts" :key="post.id" :title="post.title" :text="post.body"/>
      </div>
      
      <span class="p-5"></span>

      <!-- Right side of the page -->
      <div class="hidden lg:block w-1/4 bg-orange-400 shadow-lg space-y-5 p-5">
        <IndexCard year=2020 month='Dec' @filterMonth="filterMonthYear(arguments)"/>
        <IndexCard year=2019 month='Dec'/>
      </div>
    </div>

  </div>
</template>

<script>
import PostCard from '@/components/PostCard';
import IndexCard from '@/components/IndexCard';
import postData from '@/assets/data/data.json';

export default {
  methods: {
    filterMonthYear: function(arrArg) {
      var mth = arrArg[0]
      var yr = arrArg[1]
      console.log("Index caught filterMonthYear")
    },
  },
  data() {
    return {
      posts: postData
    }
  },
  components: {
    PostCard,
    IndexCard
  }
}
</script>

<style scoped>
</style>
