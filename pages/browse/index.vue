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
          class="w-full mb-4 sm:w-2/3 sm:mb-0 sm:mr-4"
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
  </div>
</template>

<script>
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
      ]
    }
  }
}
</script>
