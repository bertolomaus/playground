<script lang="ts" setup>

const { data, error } = await useAsyncData('index', async () => {
  const response = await fetch('http://localhost:1337/api/index')
  return await response.json()
})

</script>

<template>
  <div>
    <h2>Strapi Articles</h2>
    <pre>
      {{ data }}
    </pre>
  </div>
</template>