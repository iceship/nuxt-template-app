<script setup lang="ts">
const colorMode = useColorMode();

const isLight = computed({
  get() {
    return colorMode.value === "light";
  },
  set(value) {
    colorMode.preference = value ? "light" : "dark";
  },
});
</script>

<template>
  <label class="swap swap-rotate mx-4">
    <input v-model="isLight" type="checkbox">
    <Icon
      name="tabler:moon-filled"
      class="swap-on"
      size="24"
    />
    <Icon
      name="tabler:sun"
      class="swap-off"
      size="24"
    />
  </label>
</template>
