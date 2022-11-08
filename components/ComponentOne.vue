
<template>
  <div>
    Component: {{ foo }}
  </div>
</template>
<script lang="ts" setup>
  import {ComponentObjectPropsOptions} from "vue";

  interface Props {
    foo: string
    bar?: number
  }

  const props = defineProps<ComponentObjectPropsOptions<Props>>({
    foo: {
      type: String, 
      required: true,
      validator(value: unknown): boolean {
        return true
      }
    },
    bar: Number
  })
</script>

<style scoped></style>
