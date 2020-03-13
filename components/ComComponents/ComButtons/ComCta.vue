<template>
  <button
    type="button"
    class="border px-4 py-2 rounded-lg font-bold focus:outline-none"
    :class="[
      `border-${colour}-500 text-${colour}-500 hover:bg-${colour}-200`,
      {
        'bg-teal-100': solid && colour === 'teal',
        'bg-yellow-100': solid && colour === 'yellow'
      }
    ]"
    v-on="$listeners"
  >
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: {
    colour: {
      type: String,
      default: 'teal'
    },
    solid: Boolean
  }
}
</script>
