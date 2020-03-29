<template>
  <modal
    name="thankYouModal"
    classes="bg-white rounded-2xl"
    transition="pop-up"
    height="auto"
    @before-open="handleClose"
    adaptive
  >
    <div class="p-12">
      <div class="flex flex-col justify-center items-center">
        <object class="h-48 pb-6" :data="thankYouSvg" type="image/svg+xml">
        </object>
        <h3>
          {{ thankYouMessage }}
        </h3>
      </div>
    </div>
  </modal>
</template>

<script>
import thankYouSvg from '~/assets/images/thank_you.svg'

export default {
  props: {
    thankYouMessage: {
      type: String,
      required: true
    }
  },
  data() {
    return {
      thankYouSvg
    }
  },
  methods: {
    handleClose() {
      setTimeout(() => {
        this.$modal.hide('thankYouModal')
      }, 3000)
    }
  }
}
</script>
