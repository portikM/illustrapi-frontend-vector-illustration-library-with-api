<template>
  <div class="relative">
    <multiselect
      v-model="value"
      :class="{ 'shadow-lg': open }"
      class="absolute text-gray-600 bg-gray-100 border border-gray-300 rounded-lg px-4 py-2 block w-full appearance-none leading-normal focus:outline-none focus:shadow-outline"
      :options="options"
      :placeholder="placeholder"
      multiple
      searchable
      :close-on-select="false"
      :clear-on-select="false"
      @open="open = true"
      @close="open = false"
    >
      <template slot="placeholder">
        <span class="text-gray-500">{{ placeholder }}</span>
      </template>

      <!-- tag (hidden) -->
      <template slot="tag" slot-scope="props">
        <span class="hidden">
          {{ props.option }}
        </span>
      </template>

      <!-- option -->
      <template slot="option" slot-scope="props">
        <span>
          {{ props.option }}
        </span>
      </template>

      <!-- selection (items counter) -->
      <template slot="selection" slot-scope="{ values, isOpen }">
        <span v-if="values.length && !isOpen">
          {{ values.length }} categories selected
        </span>
      </template>

      <!-- caret -->
      <template slot="caret">
        <span
          v-if="!open"
          class="text-gray-400 absolute right-0 top-0 mr-3 mt-4"
        >
          <!-- prettier-ignore -->
          <svg width="14" height="8" fill="none" xmlns="http://www.w3.org/2000/svg" class="stroke-current">
            <path d="M1 1l6 6 6-6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
          </svg>
        </span>
      </template>
    </multiselect>
  </div>
</template>

<script>
import Multiselect from 'vue-multiselect'
import * as _ from 'lodash'

export default {
  components: { Multiselect },
  props: {
    selected: {
      type: Array,
      default: null
    },
    options: {
      type: Array,
      required: true
    },
    placeholder: {
      type: String,
      default: 'Select options'
    }
  },
  data() {
    return {
      value: null,
      open: false
    }
  },
  methods: {
    // eslint-disable-next-line arrow-parens
    throttledUpdate: _.debounce((vm) => {
      vm.$emit('input', vm.value)
    }, 500)
  },
  watch: {
    value: {
      handler(val) {
        if (val) {
          this.throttledUpdate(this)
        }
      }
    }
  },
  created() {
    this.value = this.selected
  }
}
</script>

<style lang="scss">
.multiselect__input {
  &:focus {
    @apply outline-none bg-transparent;
  }
}

.multiselect__content {
  @apply w-full;
}

.multiselect__element .multiselect__option {
  @apply w-full cursor-pointer;

  &::before {
    font-family: 'Font Awesome 5 Pro';
    font-weight: 400;
    content: '\f111';
    @apply text-gray-400;
  }

  &.multiselect__option--selected {
    &::before {
      font-family: 'Font Awesome 5 Pro';
      font-weight: 900;
      content: '\f058';
      @apply text-teal-500;
    }
  }
}
</style>
