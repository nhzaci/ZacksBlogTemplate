<template>
  <div class="min-h-screen items-stretch">
    <NavBar />
    <nuxt />
  </div>
</template>

<script>
import NavBar from '@/components/NavBar';

export default {
  components: {
    NavBar
  }
}
</script>

<style>
</style>
