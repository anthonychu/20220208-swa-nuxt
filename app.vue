<template>
  <div>
    <div>{{ data }}</div>
    <NuxtWelcome />
  </div>
</template>

<script setup>
const { data, refresh, pending } = await useAsyncData('/api/hello', () => $fetch('/api/hello'))
</script>