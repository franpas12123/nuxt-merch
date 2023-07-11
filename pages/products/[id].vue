<template>
  <div>
    <ProductDetails :product="product" />
  </div>
</template>

<script setup>
const { id } = useRoute().params

// fetch product from fakestoreapi using id
const { data: product } = await useFetch(`https://fakestoreapi.com/products/${id}`, { key: id })
</script>

<style lang="scss" scoped></style>