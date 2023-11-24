<script lang="ts" setup>
definePageMeta({
  code: "4QU4",
  stamp: "Aquarius"
})
</script>

<template>
  <div>
    Page: Aquarius
    <p>{{ $route.name }}</p>
    <p>{{ $route.meta.code }}</p>
  </div>
</template>
