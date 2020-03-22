<template>
  <div class="flex flex-col justify-center max-w-5xl mx-auto px-4 pt-16">
    <h1 class="pb-4">This is how it's gonna look</h1>
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
          />
          <ComColourPicker v-model="search.colour" class="ml-4 sm:ml-0" />
        </div>
      </div>
    </div>
    <div class="w-full flex justify-center flex-wrap pb-16">
      <div
        v-for="(illustration, n) in demoIllustrations"
        :key="n"
        class="w-56 text-center rounded-lg hover:shadow-2xl px-4 py-6 mx-2 my-6 cursor-pointer"
        @click="openIllustration(illustration.name)"
      >
        <object
          class="h-24 w-auto mx-auto mb-6 pointer-events-auto"
          :data="illustration.src"
          type="image/svg+xml"
        >
        </object>
        {{ illustration.name }}
      </div>
    </div>
  </div>
</template>

<script>
import * as _ from 'lodash'

import BusinessSvg from '~/assets/images/demo-illustrations/business.svg'
import EducationSvg from '~/assets/images/demo-illustrations/education.svg'
import FoodSvg from '~/assets/images/demo-illustrations/food.svg'
import HealthSvg from '~/assets/images/demo-illustrations/health.svg'
import HobbySvg from '~/assets/images/demo-illustrations/hobby.svg'
import NatureSvg from '~/assets/images/demo-illustrations/nature.svg'
import OfficeSvg from '~/assets/images/demo-illustrations/office.svg'
import ShoppingSvg from '~/assets/images/demo-illustrations/shopping.svg'
import TechnologySvg from '~/assets/images/demo-illustrations/technology.svg'
import TravelSvg from '~/assets/images/demo-illustrations/travel.svg'

export default {
  data() {
    return {
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
        { name: 'Business deal', category: 'Business', src: BusinessSvg },
        { name: 'Education', category: 'Education', src: EducationSvg },
        { name: 'Burger', category: 'Food', src: FoodSvg },
        { name: 'Fitness', category: 'Health', src: HealthSvg },
        { name: 'Hobby', category: 'Hobby', src: HobbySvg },
        { name: 'Environment', category: 'Nature', src: NatureSvg },
        { name: 'Work environment', category: 'Office', src: OfficeSvg },
        { name: 'Online shopping', category: 'Shopping', src: ShoppingSvg },
        {
          name: 'Software development',
          category: 'Technology',
          src: TechnologySvg
        },
        { name: 'Traveling', category: 'Travel', src: TravelSvg }
      ]
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
    }
  },
  methods: {
    handleRouteQuery() {
      const curentRouteQuery = {
        categories: this.searchCategories,
        query: this.searchQuery,
        colour: this.searchColour
      }

      if (curentRouteQuery !== this.search) {
        if (this.searchCategories) {
          this.search.categories = this.searchCategories
        }
        if (this.searchQuery) {
          this.search.query = this.searchQuery
        }
        if (this.searchColour) {
          this.search.colour = this.searchColour
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

      this.$router.push({
        path: 'browse',
        query: routeQuery
      })

      this.handleSearch(this)
    },
    // eslint-disable-next-line arrow-parens
    handleSearch: _.debounce(vm => {
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

      console.log('search params: ', routeQuery)
    }, 500),
    openIllustration(illustration) {
      console.log(illustration)
    }
  },
  created() {
    this.handleRouteQuery()
  },
  watch: {
    search: {
      deep: true,
      handler(val) {
        this.executeRouteQuery()
      }
    }
  }
}
</script>
