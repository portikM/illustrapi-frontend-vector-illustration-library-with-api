<template>
  <div class="flex items-center sm:static sm:inset-auto">
    <div
      v-click-outside="
        () => {
          show = false
        }
      "
      class="relative"
    >
      <div @click="show = !show">
        <slot name="trigger"></slot>
      </div>
      <div
        v-if="show"
        class="origin-top-right absolute right-0 mt-2 w-48 rounded-md shadow-lg"
      >
        <div class="py-1 rounded-md bg-white shadow-xs">
          <slot name="dropdown"></slot>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: false
    }
  }
}
</script>
