<script setup>

  const route = useRoute()
  const item = await useItem('items', route.params.id)

  item.content = item.content.replaceAll('width="560" height="315"', 'class="w-full aspect-video"')

</script>

<template>
  <div class="sans-serif pt-6">
    <Prose>
      <h2>{{ item.title }}</h2>
      <p></p>
    </Prose>
    <Prose v-html="item.content" class="max-w-none prose-img:m-0 prose-img:sm:m-0 prose-img:md:m-0 prose-img:lg:m-0 prose-img:xl:m-0" />
  </div>
</template>