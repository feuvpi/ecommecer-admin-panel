<template>
  <div>
    <Navbar />
    <Products />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Navbar from '@/components/Navbar.vue'
import Tutorial from '@/components/Tutorial.vue'
import Products from '@/pages/products/index.vue'

export default Vue.extend({
  name: 'IndexPage',
  components: {
    Navbar,
    Products,
    Tutorial
  }
})
</script>

