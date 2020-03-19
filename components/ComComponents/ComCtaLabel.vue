<template>
  <span
    class="block px-3 py-2 text-xs font-black uppercase border rounded-lg"
    :class="`bg-${colour}-100 border-${colour}-500 text-${colour}-500`"
  >
    <slot></slot>
  </span>
</template>

<script>
export default {
  props: {
    colour: {
      type: String,
      default: 'yellow'
    }
  }
}
</script>
