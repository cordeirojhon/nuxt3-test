<template>
  <div class="p-4 flex justify-center content-start">
    <component
      v-for="(block, index) in configpage['page01'].blocks"
      :key="index"
      :is="components[block.name]"
      v-bind="block"
      :customData="block.data"
    >
    </component>
  </div>
</template>
<script setup>

  const components = {
    ComponentOne: resolveComponent('ComponentOne'),
    ComponentTwo: resolveComponent('ComponentTwo')
  }

  const { data: configpage } = await useFetch('http://127.0.0.1:3001/api/config.json', { pick: ['page01'] });

</script>

<style>
  :root{
    --custom-color-title: red
  }
  .custom-color-title{color: var(--custom-color-title)}
</style>