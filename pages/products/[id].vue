<template>
  <div>
    <ProductDetails :product="product" />
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'products'
})

const { id } = useRoute().params

// fetch product from fakestoreapi using id
const { data: product } = await useFetch(`https://fakestoreapi.com/products/${id}`, { key: id })
if (!product.value) {
  throw createError({
    statusCode: 404,
    statusMessage: 'Product not found',
    fatal: true
  })
}
</script>

<style lang="scss" scoped></style>