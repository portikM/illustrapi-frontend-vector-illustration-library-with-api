<template>
  <button
    type="button"
    :disabled="disabled"
    class="border px-4 py-2 rounded-lg font-bold focus:outline-none hover:bg-gray-200 focus:bg-gray-200"
    :class="{ 'text-gray-400 cursor-not-allowed': disabled }"
    v-on="$listeners"
  >
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: {
    disabled: {
      type: Boolean,
      default: false
    }
  }
}
</script>
