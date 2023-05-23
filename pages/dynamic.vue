<template>
    <div class="p-4">
    Custom layout defined dynamically with the <code>NuxtLayout</code> component
    <br>
    <NuxtLayout :name="layout">
      Default slot
      <br>
      <button class="border p-1 rounded" @click="layout = layout ? null : 'custom'">
        Switch layout
      </button>
{{ dd }}
      <template #header>
        Header slot
      </template>
    </NuxtLayout>
    <br>
    <NuxtLink to="/">
      Back to home
    </NuxtLink>
  </div>
</template>

<script>
definePageMeta({
  layout: false
})
export default {
  data: () => ({
    layout: 'custom',

    tt: 'z',
    dd:'xxx'
  })
}
</script>