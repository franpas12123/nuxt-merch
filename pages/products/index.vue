<template>
  <div class="">
    <div class="grid grid-cols-4 gap-5">
      <div v-for="product in products" :key="`p-${product.id}-${product?.title}`">
        <ProductCard :product="product" />
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'products'
})

// fetch products from fakestore api
const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>

<!-- <style scoped></style> -->