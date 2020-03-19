<template>
  <div>
    <input
      class="bg-gray-100 border border-gray-300 rounded-lg px-4 py-2 block w-full appearance-none leading-normal focus:outline-none focus:shadow-outline"
      :type="type"
      :placeholder="placeholder"
      :value="value"
      @keypress.enter="$emit('enter')"
      @input="$emit('input', $event.target.value)"
    />
  </div>
</template>

<script>
export default {
  props: {
    type: {
      type: String,
      default: 'text'
    },
    placeholder: {
      type: String,
      default: 'Start typing'
    },
    value: {
      type: [String, Number],
      default: ''
    }
  }
}
</script>
