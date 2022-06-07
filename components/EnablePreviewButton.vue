<template>
  <div class="inline-flex rounded-md shadow">
    <button
      class="
        inline-flex
        items-center
        justify-center
        px-5
        py-3
        border border-transparent
        text-base
        font-medium
        rounded-md
        text-white
        bg-indigo-600
        hover:bg-indigo-700
      "
      @click="toggle"
    >
      {{ text }}
    </button>
  </div>
</template>

<script>
export default {
  computed: {
    text() {
      return this.$preview ? "Disable Preview" : "Enable Preview";
    },
  },
  methods: {
    toggle() {
      this.$preview ? this.disable() : this.enable();
    },
    enable() {
      window.location.assign(window.location.href + "?preview=1");
    },
    disable() {
      window.location.assign(window.location.origin + window.location.pathname);
    },
  },
};
</script>