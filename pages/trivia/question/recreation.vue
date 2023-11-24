<script lang="ts" setup>
definePageMeta({
  code: "F15H",
  stamp: "picture of angling"
})
</script>

<template>
  <div>
    Page: Recreation
    <p>{{ $route.name }}</p>
    <p>{{ $route.meta.code }}</p>
  </div>
</template>
