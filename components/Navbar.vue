<template>
  <nav class="bg-slate-300 shadow">
    <div class="container mx-auto px-4 py-3">
      <div class="flex justify-between items-center">
        <div class="flex-grow">
          <nuxt-link class="text-xl font-bold text-gray-900" to="/">SHOP - ADMIN</nuxt-link>
        </div>
        <div class="flex items-center justify-items-center">
          <div class="relative mx-auto">
            <input
              class="w-96 place-self-center justify-self-center w-200 border rounded-full py-2 px-3 bg-gray-100 focus:outline-none focus:ring-2 focus:ring-orange-600 focus:border-transparent"
              type="text"
              placeholder="Procurar...">
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>
