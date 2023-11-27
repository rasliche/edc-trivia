<script lang="ts" setup>
definePageMeta({
  code: "M4NG",
  stamp: "mangroves"
})
</script>

<template>
  <div>
    Page: mangroves
    <p>What services do mangroves provide?</p>
    
    <p>{{ $route.name }}</p>
    <p>{{ $route.meta.code }}</p>
  </div>
</template>
