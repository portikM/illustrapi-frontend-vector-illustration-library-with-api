<template>
  <div v-click-outside="close" class="relative p-12">
    <ComTimes class="absolute top-0 right-0 mt-12 mr-12" @click="close" />
    <div class="flex flex-col justify-center items-center">
      <div v-if="id === 'business-deal'" class="w-56 text-center rounded-lg">
        <h3 class="pb-4">
          Business deal
        </h3>
        <Business class="mb-10 h-48" :colour="colour" />
      </div>

      <div v-if="id === 'education'" class="w-56 text-center rounded-lg">
        <h3 class="pb-4">
          Education
        </h3>
        <Education class="mb-10 h-48" :colour="colour" />
      </div>

      <div v-if="id === 'burger'" class="w-2/3 text-center rounded-lg">
        <h3 class="pb-4">
          Burger
        </h3>
        <Food class="mb-10 h-48" :colour="colour" />
      </div>

      <div v-if="id === 'fitness'" class="w-56 text-center rounded-lg">
        <h3 class="pb-4">
          Fitness
        </h3>
        <Health class="mb-10 h-48" :colour="colour" />
      </div>

      <div v-if="id === 'hobby'" class="w-56 text-center rounded-lg">
        <h3 class="pb-4">
          Hobby
        </h3>
        <Hobby class="mb-10 h-48" :colour="colour" />
      </div>

      <div v-if="id === 'environment'" class="w-56 text-center rounded-lg">
        <h3 class="pb-4">
          Environment
        </h3>
        <Nature class="mb-10 h-48" :colour="colour" />
      </div>

      <div v-if="id === 'work-environment'" class="w-56 text-center rounded-lg">
        <h3 class="pb-4">
          Work environment
        </h3>
        <Office class="mb-10 h-48" :colour="colour" />
      </div>

      <div v-if="id === 'online-shopping'" class="w-56 text-center rounded-lg">
        <h3 class="pb-4">
          Online shopping
        </h3>
        <Shopping class="mb-10 h-48" :colour="colour" />
      </div>

      <div
        v-if="id === 'software-development'"
        class="w-56 text-center rounded-lg"
      >
        <h3 class="pb-4">
          Software development
        </h3>
        <Technology class="mb-10 h-48" :colour="colour" />
      </div>

      <div v-if="id === 'traveling'" class="w-56 text-center rounded-lg">
        <h3 class="pb-4">
          Traveling
        </h3>
        <Travel class="mb-10 h-48" :colour="colour" />
      </div>

      <span
        class="relative block w-full pl-4 pr-12 py-2 mb-4 bg-gray-800 text-green-400 rounded-lg font-mono truncate"
      >
        https://api.illustrapi.com/il?name={{ id }}&#x26;token=YOUR_ACCESS_TOKEN
        <button
          class="p-1 absolute top-0 right-0 mr-2 mt-1 hover:text-gray-300 focus:outline-none focus:text-gray-300"
          v-tooltip="{
            content:
              'Once we release our API, you can look up any illustration here',
            classes:
              'bg-gray-800 text-white w-64 px-2 py-1 rounded-lg text-sm mb-3 z-1000'
          }"
        >
          <!-- prettier-ignore -->
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            fill="none"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="stroke-current text-white"
          >
            <circle cx="12" cy="12" r="10" />
            <path d="M9.09 9a3 3 0 015.83 1c0 2-3 3-3 3M12 17h.01" />
          </svg>
        </button>
      </span>

      <div class="w-full flex justify-center sm:justify-end">
        <span
          v-tooltip.bottom="{
            content:
              'Downloading along with Figma components will be available once we announce the official release',
            classes:
              'bg-gray-800 text-white w-64 px-2 py-1 rounded-lg text-sm mt-3 z-1000'
          }"
        >
          <ComTransparentButton class="mr-3 inline-flex items-center" disabled>
            <svg
              width="16"
              height="18"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
              class="stroke-current mr-2"
            >
              <path
                d="M1 13v2.4c0 .8837.69645 1.6 1.55556 1.6H13.4444C14.3036 17 15 16.2837 15 15.4V13M5 9l3 3 3-3M8 1v11"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
            Download
          </ComTransparentButton>
        </span>
        <ComCta
          v-clipboard:copy="shareLink"
          v-clipboard:success="onCopy"
          v-clipboard:error="onError"
          class="inline-flex items-center"
          solid
        >
          <svg
            width="14"
            height="17"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            class="stroke-current mr-2"
          >
            <path
              d="M1 8v6.4c0 .8837.67157 1.6 1.5 1.6h9c.8284 0 1.5-.7163 1.5-1.6V8M10 4L7 1 4 4M7 1v10"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
          Share
        </ComCta>
      </div>
    </div>
  </div>
</template>

<script>
import Business from '~/components/DemoIllustrations/Business.vue'
import Education from '~/components/DemoIllustrations/Education.vue'
import Food from '~/components/DemoIllustrations/Food.vue'
import Health from '~/components/DemoIllustrations/Health.vue'
import Hobby from '~/components/DemoIllustrations/Hobby.vue'
import Nature from '~/components/DemoIllustrations/Nature.vue'
import Office from '~/components/DemoIllustrations/Office.vue'
import Shopping from '~/components/DemoIllustrations/Shopping.vue'
import Technology from '~/components/DemoIllustrations/Technology.vue'
import Travel from '~/components/DemoIllustrations/Travel.vue'

export default {
  components: {
    Business,
    Education,
    Food,
    Health,
    Hobby,
    Nature,
    Office,
    Shopping,
    Technology,
    Travel
  },
  props: {
    id: {
      type: String,
      required: true
    },
    colour: {
      type: String,
      default: '#38B2AC'
    }
  },
  computed: {
    shareLink() {
      let queryCategories = ''
      let queryQuery = ''
      let queryColour = ''

      if (this.$route.query.categories) {
        // eslint-disable-next-line arrow-parens
        const a = this.$route.query.categories.map((category) => `${category}&`)
        queryCategories = `categories=${a.join('categories=')}`
      }

      if (this.$route.query.query) {
        queryQuery = `query=${this.$route.query.query}&`
      }

      if (this.$route.query.colour) {
        queryColour = `colour=${this.$route.query.colour.replace('#', '%23')}&`
      }

      return `${process.env.BASE_URL +
        '/browse?' +
        queryCategories +
        queryQuery +
        queryColour +
        'view=' +
        this.id}`
    }
  },
  methods: {
    close() {
      this.$emit('close')
    },
    onCopy() {
      this.$ga.event('Share Illustration', 'copy', this.id)
      this.$notify({
        group: 'notif',
        type: 'success',
        text: 'Copied to clipboard!'
      })
    },
    onError() {
      this.$notify({
        group: 'notif',
        type: 'error',
        text:
          'Sorry, an error occurred.<br>Please let as know at help@illustrapi.com'
      })
    }
  }
}
</script>
