<template>
    <div class="mt-2 mx-2">
        <div class="p mx-2 font-bold text-2xl mt-4">CADASTRO DE PRODUTOS</div>
        <div v-show="!products.length" class="bg-blue-100 border-t border-b border-blue-500 text-blue-700 px-4 py-3 mt-2" role="alert">
            <p class="font-bold">Carregando!</p>
            <p class="text-sm">Estamos buscando as melhores ofertas...</p>
        </div>
        <div class="flex-row gap-4" v-if="products.length > 0">
            <Product v-for="product in products" :key="product.id" :product="product" />
        </div>
    </div>
</template>

<script>
import Product from './product'
export default {
    layout: ({ isMobile }) => isMobile ? 'mobile' : 'default',
    components: { Product },
    computed: {
        products() { 
            return this.$store.getters['products/products']
        }
    },
    mounted() {
        this.$store.dispatch('products/fetchProducts')
    },
    methods: {
    },
}
</script>