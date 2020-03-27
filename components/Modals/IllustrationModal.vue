<template>
  <div v-click-outside="close">
    {{ id }}
    <button @click="close">close</button>
  </div>
</template>

<script>
export default {
  props: {
    id: {
      type: String,
      required: true
    }
  },
  methods: {
    close() {
      this.$emit('close')
    }
  }
}
</script>
