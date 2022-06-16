<script setup>
  const route = useRoute()
  const item = await useItem('items', route.params.id)

  console.log(item)
</script>

<template>
  <div class="sans-serif">
    <h2>{{ item.title }}</h2>
  </div>
</template>