<template>
  <div class="flex flex-col justify-center max-w-5xl mx-auto px-4 py-10">
    <h1 class="pb-4">Beautiful vector illustration library with API</h1>
    <p class="text-center pb-16">
      Simple and delightful design solution that will make your next project
      look awesome.
    </p>
    <section class="relative flex justify-between">
      <div class="p-4 w-11/12 sm:w-10/12 bg-gray-800 rounded-lg shadow-lg">
        <div class="flex pb-3">
          <span class="block w-3 h-3 bg-red-500 rounded-full mr-2"></span>
          <span class="block w-3 h-3 bg-yellow-500 rounded-full mr-2"></span>
          <span class="block w-3 h-3 bg-green-500 rounded-full mr-2"></span>
        </div>
        <!-- prettier-ignore -->
        <code class="font-mono">
          <span class="block truncate">1&nbsp;&nbsp;<span class="text-blue-100">&#x3c;</span><span class="text-red-400">div</span><span class="text-yellow-300"> class</span><span class="text-blue-100">&#x3d;&#x22;</span><span class="text-green-400">product-card</span><span class="text-blue-100">&#x22;&#x3e;</span></span>
          <span class="block truncate">2&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-blue-100">&#x3c;</span><span class="text-red-400">header</span><span class="text-yellow-300"> class</span><span class="text-blue-100">&#x3d;&#x22;</span><span class="text-green-400">product-header</span><span class="text-blue-100">&#x22;&#x3e;</span></span>
          <span class="block truncate">3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-blue-100">&#x3c;</span><span class="text-red-400">object</span><span class="text-yellow-300"> class</span><span class="text-blue-100">&#x3d;&#x22;</span><span class="text-green-400">illustrapi</span><span class="text-blue-100">&#x22;</span></span>
          <span class="block truncate">4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-yellow-300">data</span><span class="text-blue-100">&#x3d;&#x22;</span><span class="text-green-400">https://api.illustrapi.com/name=product&#x26;token=YOUR_ACCESS_TOKEN</span><span class="text-blue-100">&#x22;</span></span>
          <span class="block truncate">5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-yellow-300">type</span><span class="text-blue-100">&#x3d;&#x22;</span><span class="text-green-400">image/svg+xml</span><span class="text-blue-100">&#x22;&#x3e;</span></span>
          <span class="block truncate">6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-blue-100">&#x3c;&#x2f;</span><span class="text-red-400">object</span><span class="text-blue-100">&#x3e;</span></span>
          <span class="block truncate">7&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-blue-100">&#x3c;&#x2f;</span><span class="text-red-400">header</span><span class="text-blue-100">&#x3e;</span></span>
          <span class="block truncate">8&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-blue-100">&#x3c;</span><span class="text-red-400">div</span><span class="text-yellow-300"> class</span><span class="text-blue-100">&#x3d;&#x22;</span><span class="text-green-400">product-description</span><span class="text-blue-100">&#x22;&#x3e;</span></span>
          <span class="block truncate">9&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-blue-100">&#x3c;</span><span class="text-red-400">h3</span><span class="text-blue-100">&#x3e;</span><span class="text-white">Lorem ipsum</span><span class="text-blue-100">&#x3c;&#x2f;</span><span class="text-red-400">h3</span><span class="text-blue-100">&#x3e;</span></span>
          <span class="block truncate">10&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-blue-100">&#x3c;</span><span class="text-red-400">p</span><span class="text-blue-100">&#x3e;</span><span class="text-white">Lorem ipsum dolor sit amet.</span><span class="text-blue-100">&#x3c;&#x2f;</span><span class="text-red-400">p</span><span class="text-blue-100">&#x3e;</span></span>
          <span class="block truncate">11&nbsp;&nbsp;&nbsp;<span class="text-blue-100">&#x3c;&#x2f;</span><span class="text-red-400">div</span><span class="text-blue-100">&#x3e;</span></span>
          <span class="block truncate">12&nbsp;<span class="text-blue-100">&#x3c;&#x2f;</span><span class="text-red-400">div</span><span class="text-blue-100">&#x3e;</span></span>
        </code>
      </div>
      <div
        class="absolute right-0 bottom-0 -mb-56 sm:-mb-40 w-11/12 sm:w-1/3 bg-gray-100 rounded-lg shadow-lg"
      >
        <header class="rounded-t-lg border-t-8 border-teal-500">
          <div class="p-8 text-center">
            <object
              class="pb-4 w-10/12 mx-auto"
              :data="productDemoSvg"
              type="image/svg+xml"
            ></object>
            <h3>Lorem ipsum</h3>
            <p>Lorem ipsum dolor sit amet.</p>
          </div>
        </header>
      </div>
    </section>
    <div class="h-screen"></div>
  </div>
</template>

<script>
import productDemoSvg from '~/assets/images/product_demo.svg'

export default {
  head() {
    return {
      title: 'illustrapi - vector illustration library',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Beautiful vector illustration library with API.'
        },
        {
          hid: 'keywords',
          name: 'keywords',
          content: 'illustrapi, vector, illustration, library, API, svg'
        }
      ]
    }
  },
  data() {
    return {
      productDemoSvg
    }
  }
}
</script>

<style></style>
