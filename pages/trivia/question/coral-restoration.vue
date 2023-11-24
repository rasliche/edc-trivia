<script lang="ts" setup>
definePageMeta({
  code: "C4RL",
  stamp: "coral tree"
})
</script>

<template>
  <div>
    Page: Coral Restoration
    <p>{{ $route.name }}</p>
    <p>{{ $route.meta.code }}</p>
  </div>
</template>
