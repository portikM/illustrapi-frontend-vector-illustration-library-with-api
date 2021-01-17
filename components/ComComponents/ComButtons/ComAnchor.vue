<template>
  <a
    :href="href"
    :target="target"
    class="border px-4 py-2 rounded-lg font-bold focus:outline-none"
    :class="[
      `border-${colour}-500 text-${colour}-500 hover:bg-${colour}-200 focus:bg-${colour}-200`,
      {
        'bg-teal-100': solid && colour === 'teal',
        'bg-yellow-100': solid && colour === 'yellow'
      }
    ]"
    v-on="$listeners"
  >
    <slot></slot>
  </a>
</template>

<script>
export default {
  props: {
    href: {
      type: String,
      required: true
    },
    target: {
      type: String,
      default: '_self'
    },
    colour: {
      type: String,
      default: 'teal'
    },
    solid: Boolean
  }
}
</script>
