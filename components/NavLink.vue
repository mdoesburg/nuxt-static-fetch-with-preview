<template>
  <NuxtLink
    class="
      inline-flex
      items-center
      justify-center
      px-5
      py-2
      border border-transparent
      text-base
      font-medium
      rounded-md
      text-white
      bg-indigo-600
      hover:bg-indigo-700
      mr-3
    "
    active-class="bg-indigo-900"
    exact-path
    v-bind="$attrs"
  >
    <slot />
  </NuxtLink>
</template>