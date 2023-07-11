<template>
  <div class="card text-center">
    <img :src="product.image" alt="thumb" class="max-h-32 my-0 mx-auto max-w-[70%]">
    <p class="font-bold text-gray-500 m-4 truncate">{{ product.title }}</p>
    <NuxtLink :to="`/products/${product.id}`">
      <p class="btn my-4">View Details</p>
    </NuxtLink>
  </div>
</template>

<script setup>
const { product } = defineProps(['product'])
</script>

<style lang="scss" scoped></style>