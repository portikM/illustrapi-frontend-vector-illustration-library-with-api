<template>
  <div class="px-4 pt-16">
    <div class="flex flex-col justify-center max-w-5xl mx-auto">
      <h1 class="pb-4">
        This is how it's gonna look
      </h1>
      <div class="flex justify-between pb-16">
        <div class="w-full flex flex-wrap sm:flex-no-wrap">
          <ComMultiselect
            v-model="search.categories"
            :selected="search.categories"
            :options="categories"
            placeholder="Categories"
            class="w-full mb-16 sm:w-2/3 sm:mb-0 sm:mr-4 z-50"
          />
          <div class="w-full flex justify-between items-center">
            <ComInput
              v-model="search.query"
              class="w-full sm:w-2/3"
              placeholder="Search"
            >
              <!-- prettier-ignore -->
              <svg
                slot="icon"
                width="19"
                height="19"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                class="stroke-current origin-center"
              >
                <path clip-rule="evenodd" d="M8 15c3.866 0 7-3.134 7-7 0-3.86599-3.134-7-7-7-3.86599 0-7 3.13401-7 7 0 3.866 3.13401 7 7 7z" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                <path d="M18 18l-5-5" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
              </svg>
            </ComInput>
            <ComColourPicker
              v-model="search.colour"
              :colour="searchColour"
              class="ml-4 sm:ml-0"
            />
          </div>
        </div>
      </div>
    </div>
    <div v-if="loading">
      <div class="h-48"></div>
      <div class="h-48"></div>
    </div>
    <section v-else>
      <div class="flex justify-center max-w-5xl mx-auto pb-16">
        <div
          v-if="!filteredResults.length"
          class="w-full flex flex-col justify-center text-center"
        >
          <object
            class="h-64 w-auto pb-4"
            :data="searchEmptySvg"
            type="image/svg+xml"
          >
          </object>
          <p>Sorry, no results</p>
        </div>
        <div
          class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4"
        >
          <div
            v-if="
              filteredResults.some((result) => result.name === 'Business deal')
            "
            @click="viewIllustration('business-deal')"
            class="w-56 text-center rounded-lg hover:shadow-2xl px-4 py-6 cursor-pointer"
          >
            <Business class="pb-4 h-32" :colour="searchColour" />
            <p>Business deal</p>
          </div>

          <div
            v-if="filteredResults.some((result) => result.name === 'Education')"
            @click="viewIllustration('education')"
            class="w-56 text-center rounded-lg hover:shadow-2xl px-4 py-6 cursor-pointer"
          >
            <Education class="pb-4 h-32" :colour="searchColour" />
            <p>Education</p>
          </div>

          <div
            v-if="filteredResults.some((result) => result.name === 'Burger')"
            @click="viewIllustration('burger')"
            class="w-56 text-center rounded-lg hover:shadow-2xl px-4 py-6 cursor-pointer"
          >
            <Food class="pb-4 h-32" :colour="searchColour" />
            <p>Burger</p>
          </div>

          <div
            v-if="filteredResults.some((result) => result.name === 'Fitness')"
            @click="viewIllustration('fitness')"
            class="w-56 text-center rounded-lg hover:shadow-2xl px-4 py-6 cursor-pointer"
          >
            <Health class="pb-4 h-32" :colour="searchColour" />
            <p>Fitness</p>
          </div>

          <div
            v-if="filteredResults.some((result) => result.name === 'Hobby')"
            @click="viewIllustration('hobby')"
            class="w-56 text-center rounded-lg hover:shadow-2xl px-4 py-6 cursor-pointer"
          >
            <Hobby class="pb-4 h-32" :colour="searchColour" />
            <p>Hobby</p>
          </div>

          <div
            v-if="
              filteredResults.some((result) => result.name === 'Environment')
            "
            @click="viewIllustration('environment')"
            class="w-56 text-center rounded-lg hover:shadow-2xl px-4 py-6 cursor-pointer"
          >
            <Nature class="pb-4 h-32" :colour="searchColour" />
            <p>Environment</p>
          </div>

          <div
            v-if="
              filteredResults.some(
                (result) => result.name === 'Work environment'
              )
            "
            @click="viewIllustration('work-environment')"
            class="w-56 text-center rounded-lg hover:shadow-2xl px-4 py-6 cursor-pointer"
          >
            <Office class="pb-4 h-32" :colour="searchColour" />
            <p>Work environment</p>
          </div>

          <div
            v-if="
              filteredResults.some(
                (result) => result.name === 'Online shopping'
              )
            "
            @click="viewIllustration('online-shopping')"
            class="w-56 text-center rounded-lg hover:shadow-2xl px-4 py-6 cursor-pointer"
          >
            <Shopping class="pb-4 h-32" :colour="searchColour" />
            <p>Online shopping</p>
          </div>

          <div
            v-if="
              filteredResults.some(
                (result) => result.name === 'Software development'
              )
            "
            @click="viewIllustration('software-development')"
            class="w-56 text-center rounded-lg hover:shadow-2xl px-4 py-6 cursor-pointer"
          >
            <Technology class="pb-4 h-32" :colour="searchColour" />
            <p>Software development</p>
          </div>

          <div
            v-if="filteredResults.some((result) => result.name === 'Traveling')"
            @click="viewIllustration('traveling')"
            class="w-56 text-center rounded-lg hover:shadow-2xl px-4 py-6 cursor-pointer"
          >
            <Travel class="pb-4 h-32" :colour="searchColour" />
            <p>Traveling</p>
          </div>
        </div>
      </div>
    </section>
    <div v-if="filteredResults.length < 4" class="h-48 hidden sm:block"></div>

    <modal name="illustrationModal" transition="pop-up" :clickToClose="false">
      <IllustrationModal
        v-if="viewQuery"
        :id="viewQuery"
        @close="modalCloseHandler"
      />
    </modal>
  </div>
</template>

<script>
import * as _ from 'lodash'
import searchEmptySvg from '~/assets/images/search_empty.svg'
import IllustrationModal from '~/components/Modals/IllustrationModal.vue'

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
    IllustrationModal,
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
  data() {
    return {
      loading: true,
      search: {
        categories: null,
        query: '',
        colour: '#38B2AC'
      },
      categories: [
        'Business',
        'Education',
        'Food',
        'Health',
        'Hobby',
        'Nature',
        'Office',
        'Shopping',
        'Technology',
        'Travel'
      ],
      demoIllustrations: [
        { name: 'Business deal', category: 'Business' },
        { name: 'Education', category: 'Education' },
        { name: 'Burger', category: 'Food' },
        { name: 'Fitness', category: 'Health' },
        { name: 'Hobby', category: 'Hobby' },
        { name: 'Environment', category: 'Nature' },
        { name: 'Work environment', category: 'Office' },
        { name: 'Online shopping', category: 'Shopping' },
        {
          name: 'Software development',
          category: 'Technology'
        },
        { name: 'Traveling', category: 'Travel' }
      ],
      searchResults: [],
      searchEmptySvg
    }
  },
  computed: {
    searchCategories() {
      return this.$route.query.categories
    },
    searchQuery() {
      return this.$route.query.query
    },
    searchColour() {
      return this.$route.query.colour || this.search.colour
    },
    filteredByCategory() {
      if (this.searchCategories) {
        return this.demoIllustrations.filter((illustration) => {
          if (this.searchCategories.includes(illustration.category)) {
            return { name: illustration.name, category: illustration.category }
          }
        })
      }
      return this.demoIllustrations
    },
    filteredResults() {
      if (!this.searchCategories) {
        return this.searchResults
      }
      if (!this.searchQuery && this.searchCategories) {
        return this.filteredByCategory
      }
      return this.searchResults.filter((result) => {
        if (this.searchCategories.includes(result.category)) {
          return result
        }
      })
    },
    viewQuery() {
      return this.$route.query.view
    }
  },
  methods: {
    handleRouteQuery() {
      const curentRouteQuery = {
        categories:
          typeof this.searchCategories === 'string'
            ? [this.searchCategories]
            : this.searchCategories,
        query: this.searchQuery,
        colour: this.searchColour
      }

      if (curentRouteQuery !== this.search) {
        if (this.searchCategories) {
          this.$set(
            this.search,
            'categories',
            typeof this.searchCategories === 'string'
              ? [this.searchCategories]
              : this.searchCategories
          )
        }
        if (this.searchQuery) {
          this.$set(this.search, 'query', this.searchQuery)
        }
        if (this.searchColour) {
          this.$set(this.search, 'colour', this.searchColour)
        }
      }

      this.executeRouteQuery()
    },
    executeRouteQuery() {
      // eslint-disable-next-line prefer-const
      let routeQuery = {}

      if (
        Array.isArray(this.search.categories) &&
        this.search.categories.length
      ) {
        routeQuery.categories = this.search.categories
      }
      if (this.search.query) {
        routeQuery.query = this.search.query
      }
      if (this.search.colour) {
        routeQuery.colour = this.search.colour
      }
      if (this.viewQuery) {
        routeQuery.view = this.viewQuery
      }

      this.$router.push({
        route: 'browse',
        query: routeQuery
      })

      this.handleSearch(this)
    },
    // eslint-disable-next-line arrow-parens
    handleSearch: _.debounce((vm) => {
      // eslint-disable-next-line prefer-const
      let routeQuery = {}

      if (typeof vm.searchCategories !== 'undefined') {
        routeQuery.categories = vm.searchCategories
      }
      if (typeof vm.searchQuery !== 'undefined') {
        routeQuery.query = vm.searchQuery
      }
      if (typeof vm.searchColour !== 'undefined') {
        routeQuery.colour = vm.searchColour
      }

      vm.executeSearch(routeQuery)
    }, 500),
    executeSearch(searchParams) {
      if (this.viewQuery) {
        this.$modal.show('illustrationModal')
      }

      this.loading = true
      // * results per page: &hitsPerPage=number
      this.$axios
        .get(
          `https://${
            process.env.ALGOLIA_APPLICATION_ID
          }-dsn.algolia.net/1/indexes/dev_illustrapi?query=${searchParams.query ||
            ''}&x-algolia-application-id=${
            process.env.ALGOLIA_APPLICATION_ID
          }&x-algolia-api-key=${process.env.ALGOLIA_API_KEY}`
        )
        .then((response) => {
          this.loading = false
          this.$set(this, 'searchResults', response.data.hits)
        })
        .catch((e) => {
          console.error(e)
        })
    },
    viewIllustration(id) {
      // eslint-disable-next-line prefer-const
      let routeQuery = {}

      if (
        Array.isArray(this.search.categories) &&
        this.search.categories.length
      ) {
        routeQuery.categories = this.search.categories
      }
      if (this.search.query) {
        routeQuery.query = this.search.query
      }
      if (this.search.colour) {
        routeQuery.colour = this.search.colour
      }
      routeQuery.view = id

      this.$router.push({
        route: 'browse',
        query: routeQuery
      })

      this.$modal.show('illustrationModal')
    },
    modalCloseHandler() {
      this.$modal.hide('illustrationModal')

      // eslint-disable-next-line prefer-const
      let routeQuery = {}

      if (
        Array.isArray(this.search.categories) &&
        this.search.categories.length
      ) {
        routeQuery.categories = this.search.categories
      }
      if (this.search.query) {
        routeQuery.query = this.search.query
      }
      if (this.search.colour) {
        routeQuery.colour = this.search.colour
      }

      this.$router.push({
        route: 'browse',
        query: routeQuery
      })
    }
  },
  watch: {
    search: {
      deep: true,
      handler(val) {
        this.executeRouteQuery()
      }
    },
    viewQuery: {
      immediate: true,
      handler(val) {
        if (val) {
          this.$modal.show('illustrationModal')
        }
      }
    }
  },
  created() {
    this.handleRouteQuery()
  }
}
</script>
