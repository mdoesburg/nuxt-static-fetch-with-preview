<template>
  <code :class="['bg-gray-100', 'p-1', 'rounded border', { 'text-sm': small }]">
    <slot />
  </code>
</template>

<script>
export default {
  props: {
    small: {
      type: Boolean,
      default: false,
    },
  },
};
</script>
