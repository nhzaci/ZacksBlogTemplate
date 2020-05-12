<template>
  <div class="w-screen">

    <div class="flex lg:mx-64 mx-5 mt-5">
      <!-- Left side of the page -->
      <div class="w-full lg:w-3/4 bg-orange-300 space-y-5 p-5 shadow-lg">
        <PostCard 
          v-for="blogPost in posts" 
          :key="blogPost.id" 
          :title="blogPost.title" 
          :post="blogPost.post"
          :created="blogPost.created"
          :tags="blogPost.tags"
          :imgurl="blogPost.imgurl"
        />
      </div>
      
      <span class="p-5"></span>

      <!-- Right side of the page -->
      <div class="hidden lg:block w-1/4 bg-yellow-300 shadow-lg space-y-5 p-5">
        <IndexCard year=2020 month='Dec' @filterMonth="filterMonthYear(arguments)"/>
        <IndexCard year=2019 month='Dec'/>
      </div>
    </div>

  </div>
</template>

<script>
import PostCard from '@/components/PostCard';
import IndexCard from '@/components/IndexCard';
import axios from 'axios';

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
      posts: []
    }
  },
  components: {
    PostCard,
    IndexCard
  },
  async created() {
    this.posts = await axios
      .get('http://127.0.0.1:8000/posts/')
      .then(response => response.data)
      .catch(error => console.log(error))
  }
}
</script>

<style scoped>
</style>
