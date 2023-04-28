<template>
  <div>
    <Navbar />
    <div class="flex flex-row h-screen overflow-hidden">

    <Sidebar/>
    <div class="flex-auto bg-gray-100">

      <Products />
    </div>
  </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Navbar from '@/components/Navbar.vue'
import Sidebar from '@/components/sidebar.vue'
import Products from '@/pages/products/index.vue'

export default Vue.extend({
  name: 'IndexPage',
  components: {
    Navbar,
    Products
  }
})
</script>

