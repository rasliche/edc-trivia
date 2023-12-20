<script lang="ts" setup>
  const code = ref('')
  const questionCodeExists = ref('')
  const questionRoutes = useRouter().getRoutes().filter(route => route.path.includes("question"))

  const availableCodes = questionRoutes.map(route => route.meta.code )

  watch(code, (newCode) => {
    const toRoute = questionRoutes.find(route => route.meta.code === newCode.toUpperCase())
    if (!!toRoute) {
      questionCodeExists.value = toRoute.path
      console.log(questionCodeExists)
    } else {
      questionCodeExists.value = ''
    }
  })
</script>

<template>
  <div class="max-w-xl mx-auto text-center">
    <div class="w-full">
      <p>Found a code? Scan QR code or enter the text below:</p>
      <h3>Enter Code</h3>
      <input class="block w-2/3 mx-auto border p-2 rounded" v-model="code" placeholder="M4NG" />
      <NuxtLink :to=questionCodeExists :disabled=questionCodeExists :class="[questionCodeExists ? 'bg-green-200 hover:bg-green-300 border-green-500 border-l-2-transparent border-t-2-transparent border-b-2 border-r-2 cursor-pointer' : 'bg-yellow-200 border-2 border-transparent cursor-not-allowed']" class="block w-1/4 mx-auto rounded p-2 mt-4 cursor-pointer">{{ questionCodeExists ? "Found!" : "Nothing yet..." }}</NuxtLink>
    </div>
    <section>
      <h3 class="w-full text-2xl">Stamps</h3>
      <div id="stamp-grid" class="grid gap-2 justify-items-center grid-cols-2 justify-center">
        <div v-for="question in questionRoutes" class="w-24 h-24 bg-red-300 text-center">
          {{ question.meta.stamp }}
        </div>
      </div>
    </section>
    <div class="m-24 p-2 border border-red-200">
      <h3>DEBUG</h3>
      {{ availableCodes }}
    </div>
  </div>
</template>
