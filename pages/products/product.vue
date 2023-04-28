<template>
    <div class="my-4 mx-2 border-2 border-slate-300 flex flex-row rounded-lg shadow-lg overflow-hidden">
      <div class="flex-none w-48">
        <img :src="imageUrl" alt="Product Image" class="w-full h-48 object-cover">
      </div>
      <div class="flex-auto flex flex-col justify-between p-4 bg-white">
        <h3 class="text-lg font-medium">{{ product.name }}</h3>
        <div class="flex justify-end items-center mt-4">
          <div class="mx-4 w-20 flex flex-col p-2 border-2 border-slate-300 rounded-md">
            <label for="price" class="text-gray-600 font-bold">Price</label>
            <input type="text" id="price" v-model="product.price" class="mt-1 rounded-md border-gray-300 focus:border-indigo-500 focus:ring focus:ring-indigo-200 focus:ring-opacity-50">
          </div>
          <div class="mx-4 w-20 flex flex-col p-2 border-2 border-slate-300 rounded-md">
            <label for="stock" class="text-gray-600 font-bold">Stock</label>
            <input type="text" id="stock" v-model="product.stock" class="mt-1 rounded-md border-gray-300 focus:border-indigo-500 focus:ring focus:ring-indigo-200 focus:ring-opacity-50">
          </div>
        </div>
      </div>
    </div>
  </template>

<script>
export default {
    props: ['product'],
    data() {
        return {
            successMessage: null,
            defaultImage: 'https://via.placeholder.com/150',
            errorMessage: null
        }
    },
    computed: {
    imageUrl() {
      return this.product.image_url || this.defaultImage
    },
  },
    methods: {
        addToCart(product) {
  if (product.stock > 0) {
    const cartProduct = {
      _id: product._id,
      name: product.name,
      image_url: product.image_url,
      price: product.price,
      stock: product.stock,
      quantity: 1 // Set a default quantity of 1 for the cartProduct
    }
    this.$store.dispatch('cart/addToCart', cartProduct).then(() => {
      this.$store.dispatch('products/takeFromStock', product)
      this.successMessage = 'Success!'
      setTimeout(() => { this.successMessage = null }, 3000)
    })
  } else {
    this.errorMessage = 'No items left!'
    setTimeout(() => { this.errorMessage = null }, 3000)
  }
}
    }
}


</script>

