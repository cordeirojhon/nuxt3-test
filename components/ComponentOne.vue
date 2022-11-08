<template>
  <div class="rounded overflow-hidden shadow-lg mb-4" :style="customData.style">
    <img
      class="w-full"
      :src="customData.image.url"
      alt="Sunset in the mountains"
    />
    <div class="px-6 py-4 pb-2">
      <div class="font-bold text-xl mb-2 custom-color-title">{{ customData.title }}</div>
      <p class="text-gray-700 text-base">
        {{ customData.description }}
      </p>
    </div>
    <div class="px-6 py-4">
      <span class="badge mr-2">#photography</span>
      <span class="badge mr-2">#travel</span>
      <span class="badge">#winter</span>
    </div>
  </div>
</template>

<script lang="ts" setup>
  interface Props {
    customData: object
  }

  const props = withDefaults(defineProps<Props>(), {
    customData: Object
  })
</script>

<style scoped>
  .custom-color-title{color: var(--custom-color-title)}
</style>
