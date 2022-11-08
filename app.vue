<template>
  <div>
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

  const { data: configpage } = await useFetch('http://127.0.0.1:5500/api/config.json', { pick: ['page01'] });

</script>