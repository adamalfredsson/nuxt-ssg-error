<template>
  <h1>Slug page</h1>
</template>

<script lang="ts" setup>
const { params } = useRoute();
const [slug] = params.slug as string[];
if (slug !== 'prerender') {
  throw createError({
    statusCode: 404,
    fatal: true,
  });
}
</script>
