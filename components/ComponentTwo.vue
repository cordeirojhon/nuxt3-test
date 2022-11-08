<template>
  <div>
    Component: component-one  {{customData.title}}
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

<style scoped></style>
