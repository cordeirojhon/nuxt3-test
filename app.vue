<template>
  <div>
    <component
      v-for="(block, index) in page.blocks"
      :key="index"
      :is="components[block.name]"
      v-bind="block"
      :title="data.title"
    >
    </component>
  </div>
</template>
<script setup>

  const components = {
    ComponentOne: resolveComponent('ComponentOne'),
    ComponentTwo: resolveComponent('ComponentTwo')
  }
  
  const page = {
    blocks: [
      {
        name: "ComponentOne",
        data: {
          title: 'Componente 1'
        }
      },
      {
        name: "ComponentOne",
        data: {
          title: 'Componente 2'
        }
      }
    ]
  }

</script>