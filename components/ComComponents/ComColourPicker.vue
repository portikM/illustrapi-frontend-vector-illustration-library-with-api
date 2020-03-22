<template>
  <span
    class="relative text-gray-900 flex items-center cursor-pointer"
    @click="open = !open"
    v-click-outside="() => (open = false)"
  >
    <!-- prettier-ignore -->
    <svg width="14" height="8" fill="none" xmlns="http://www.w3.org/2000/svg" class="stroke-current mr-2">
      <path d="M1 1l6 6 6-6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>

    <div
      class="block rounded-lg border border-gray-900"
      :class="size"
      :style="`background-color: ${value.hex}`"
    ></div>
    <chrome-picker
      v-if="open"
      v-model="value"
      class="absolute top-0 right-0 mt-12"
    />
  </span>
</template>

<script>
import { Chrome } from 'vue-color'
import * as _ from 'lodash'

export default {
  components: {
    'chrome-picker': Chrome
  },
  props: {
    colour: {
      type: String,
      default: '#38B2AC'
    },
    size: {
      type: String,
      default: 'w-10 h-10'
    }
  },
  data() {
    return {
      open: false,
      value: {}
    }
  },
  methods: {
    // eslint-disable-next-line arrow-parens
    throttledUpdate: _.debounce(vm => {
      vm.$emit('input', vm.value.hex)
    }, 500)
  },
  created() {
    this.value.hex = this.colour
  },
  watch: {
    value: {
      handler(val) {
        if (!_.isEmpty(val)) {
          this.throttledUpdate(this)
        }
      }
    }
  }
}
</script>
