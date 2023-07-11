<template>
  <div class="mt-7 max-w-md mx-auto text-center card">
    <p class="mt-7 text-7xl font-bold">{{ error.statusCode }}</p>
    <p class="mt-7">{{ error.message }}</p>
    <button class="btn my-7" @click="handleClearError">Go Back</button>
  </div>
</template>

<script setup>
defineProps(['error'])
const router = useRouter()
const handleClearError = () => {
  router.back()
}
</script>

<style lang="scss" scoped></style>