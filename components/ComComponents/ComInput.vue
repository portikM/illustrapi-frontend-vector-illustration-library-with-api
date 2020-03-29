<template>
  <div class="relative">
    <div
      v-if="!!$slots.icon"
      @click="$refs.input.focus()"
      class="absolute top-0 left-0 align-middle mt-3 ml-3 text-gray-400 cursor-text"
    >
      <slot name="icon"></slot>
    </div>
    <input
      :class="{ 'pl-10': !!$slots.icon, 'pr-10': !!$slots.action }"
      class="bg-gray-100 border border-gray-300 rounded-lg px-4 py-2 block w-full appearance-none leading-normal focus:outline-none focus:shadow-outline"
      :type="type"
      :placeholder="placeholder"
      :value="value"
      @keypress.enter="$emit('enter')"
      @input="input"
      ref="input"
    />
    <div
      v-if="!!$slots.icon"
      @click="$emit('action')"
      class="absolute top-0 right-0 align-middle mt-3 mr-3 text-gray-400 cursor-pointer"
    >
      <slot name="action"></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    icon: {
      type: Boolean,
      default: false
    },
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
      this.$emit('input', $event.target.value)
    }
  }
}
</script>
