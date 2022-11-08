<template>
  <figure class="md:flex bg-slate-100 rounded-xl p-8 md:p-0 dark:bg-slate-800" :style="customData.style">
    <img class="w-24 h-24 md:w-48 md:h-auto md:rounded-none rounded-full mx-auto" :src="customData.image.url" alt="" width="384" height="512">
    <div class="pt-6 md:p-8 text-center md:text-left space-y-4">
      <blockquote>
        <p class="text-lg font-medium custom-color-title">
          
        </p>
      </blockquote>
      <figcaption class="font-medium">
        <div class="text-sky-500 dark:text-sky-400">
          Sarah Dayan
        </div>
        <div class="text-slate-700 dark:text-slate-500">
          Staff Engineer, Algolia
        </div>
      </figcaption>
    </div>
  </figure>
</template>
<script lang="ts" setup>
  interface Props {
    customData: object
  }

  const props = withDefaults(defineProps<Props>(), {
    customData: Object
  });
  
</script>

<style scoped>
  .custom-color-title{color: var(--custom-color-title)}
</style>
