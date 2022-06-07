<template>
  <div
    class="
      relative
      flex
      items-top
      justify-center
      min-h-screen
      bg-gray-100
      sm:items-center sm:pt-0
    "
  >
    <div class="max-w-4xl mx-auto sm:px-6 lg:px-8">
      <div class="flex items-center justify-center">
        <NuxtLogo />
      </div>
      <div class="mt-8">
        <NavLink to="/">Home</NavLink>
        <NavLink to="/about">About</NavLink>
      </div>
      <div class="mt-8 bg-white overflow-hidden shadow sm:rounded-lg p-6">
        <h2 class="text-2xl leading-7 font-semibold">
          Test:
          <Code>enablePreview</Code>
          does not trigger component fetch
        </h2>
        <p class="mt-4 text-gray-600 leading-7">
          Click the button below and check the developer console. You wont see
          <Code small>NuxtTutorial->fetch</Code>
          printed on initial page load, but only after navigating. The page
          fetch (<Code small>IndexPage->fetch</Code> &
          <Code small>AboutPage->fetch</Code>) however, is triggered right away
          upon load.
        </p>
        <EnablePreviewButton class="mt-4" />
      </div>
    </div>
  </div>
</template>

<script>
import NuxtLogo from "./NuxtLogo.vue";
export default {
  components: { NuxtLogo },
  name: "NuxtTutorial",
  fetch() {
    console.log("NuxtTutorial->fetch");
  },
};
</script>
