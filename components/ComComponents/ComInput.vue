<template>
  <div>
    <input
      class="bg-gray-100 border border-gray-300 rounded-lg px-4 py-2 block w-full appearance-none leading-normal focus:outline-none focus:shadow-outline"
      :type="type"
      :placeholder="placeholder"
      :value="value"
      @keypress.enter="$emit('enter')"
      @input="input"
    />
  </div>
</template>

<script>
import * as _ from 'lodash'

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
  },
  methods: {
    input($event) {
      this.throttledUpdate(this, $event.target.value)
    },
    throttledUpdate: _.debounce((vm, value) => {
      vm.$emit('input', value)
    }, 500)
  }
}
</script>
