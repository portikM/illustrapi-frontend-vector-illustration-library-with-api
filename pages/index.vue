<template>
  <div class="flex flex-col justify-center max-w-5xl mx-auto px-4 pt-16">
    <ComCtaLabel class="sm:hidden mx-auto mb-2">Coming soon</ComCtaLabel>
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
    <div id="sign-up" class="pt-64 pb-32">
      <p class="text-center pt-10 pb-6">
        Sign up for project updates, early previews, and to find out when it’s
        ready.
      </p>
      <div class="flex max-w-xl mx-auto">
        <ComInput class="w-full mr-3" type="email" placeholder="Your email" />
        <ComCta class="whitespace-pre" solid>Keep me posted!</ComCta>
      </div>
    </div>
    <div class="flex flex-col w-full max-w-4xl mx-auto pb-32">
      <h2 class="pb-16">What's coming?</h2>
      <div class="w-full flex flex-col sm:flex-row sm:flex-wrap">
        <!-- beautiful -->
        <div
          class="w-full sm:w-1/2 md:w-1/3 pb-20 flex flex-col justify-center sm:justify-start text-center md:text-left"
        >
          <!-- prettier-ignore -->
          <svg width="36" height="36" fill="none" xmlns="http://www.w3.org/2000/svg" class="stroke-current text-gray-900 mb-4 mx-auto md:mx-0">
            <path d="M18 28.5L28.5 18l4.5 4.5L22.5 33 18 28.5z" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M27 19.5L24.75 8.25 3 3l5.25 21.75L19.5 27l7.5-7.5zM3 3l11.379 11.379" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M16.5 19.5c1.6569 0 3-1.3431 3-3s-1.3431-3-3-3-3 1.3431-3 3 1.3431 3 3 3z" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
          <h3 class="pb-4">Beautiful illustrations</h3>
          <p class="w-56 mx-auto md:mx-0">
            Nice, clean and crisp vector illustrations.
          </p>
        </div>

        <!-- selection -->
        <div
          class="w-full sm:w-1/2 md:w-1/3 pb-20 flex flex-col justify-center sm:justify-start text-center md:text-left"
        >
          <!-- prettier-ignore -->
          <svg width="40" height="40" fill="none" xmlns="http://www.w3.org/2000/svg" class="stroke-current text-gray-900 mb-4 mx-auto md:mx-0">
            <path
              clip-rule="evenodd"
              d="M34.7333 7.68345c-1.7192-1.72002-4.0514-2.68638-6.4833-2.68638-2.4319 0-4.7641.96636-6.4833 2.68638L20 9.45011l-1.7667-1.76666c-3.5806-3.58065-9.38599-3.58065-12.96664 0-3.58064 3.58065-3.58064 9.38605 0 12.96665l1.76667 1.7667L20 35.3834l12.9667-12.9666 1.7666-1.7667c1.72-1.7192 2.6864-4.0514 2.6864-6.4833 0-2.4319-.9664-4.76415-2.6864-6.48335z"
              stroke-width="3"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
          <h3 class="pb-4">Wide selection</h3>
          <p class="w-56 mx-auto md:mx-0">
            More than one hundred of different illustrations.
          </p>
        </div>

        <!-- API -->
        <div
          class="w-full sm:w-1/2 md:w-1/3 pb-20 flex flex-col justify-center sm:justify-start text-center md:text-left"
        >
          <!-- prettier-ignore -->
          <svg width="48" height="30" fill="none" xmlns="http://www.w3.org/2000/svg" class="stroke-current text-gray-900 mb-4 mx-auto md:mx-0">
            <path d="M32.6667 28l13-13-13-13M15.3333 2L2.33334 15 15.3333 28" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
          <h3 class="pb-4">Simple API</h3>
          <p class="w-64 mx-auto md:mx-0">
            Intuitive and well ducumented API ednpoints.
          </p>
        </div>

        <!-- searchable -->
        <div
          class="w-full sm:w-1/2 md:w-1/3 pb-20 sm:pb-0 flex flex-col justify-center sm:justify-start text-center md:text-left"
        >
          <!-- prettier-ignore -->
          <svg width="39" height="39" fill="none" xmlns="http://www.w3.org/2000/svg" class="stroke-current text-gray-900 mb-4 mx-auto md:mx-0">
            <path d="M17.875 30.875c7.1797 0 13-5.8203 13-13s-5.8203-13-13-13-13 5.8203-13 13 5.8203 13 13 13zM34.125 34.1249l-7.0688-7.0687" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
          <h3 class="pb-4">Searchable</h3>
          <p class="w-56 mx-auto md:mx-0">
            Search by collection, category and/or keywords.
          </p>
        </div>

        <!-- customizable -->
        <div
          class="w-full sm:w-1/2 md:w-1/3 pb-20 sm:pb-0 flex flex-col justify-center sm:justify-start text-center md:text-left"
        >
          <!-- prettier-ignore -->
          <svg width="39" height="39" fill="none" xmlns="http://www.w3.org/2000/svg" class="stroke-current text-gray-900 mb-4 mx-auto md:mx-0">
            <path
              d="M19.5 32.5h14.625M26.8125 5.68738c.6465-.64647 1.5233-1.00965 2.4375-1.00965.4527 0 .9009.08917 1.3192.2624.4182.17324.7982.42715 1.1183.74725.3201.3201.574.70011.7472 1.11833.1733.41823.2624.86648.2624 1.31917 0 .45269-.0891.90094-.2624 1.31917-.1732.41822-.4271.79825-.7472 1.11835L11.375 30.8749l-6.5 1.625 1.625-6.5L26.8125 5.68738z"
              stroke-width="3"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
          <h3 class="pb-4">Highly customizable</h3>
          <p class="w-56 mx-auto md:mx-0">
            Customize colour to fit your brand style.
          </p>
        </div>

        <!-- adoptable -->
        <div
          class="w-full sm:w-1/2 md:w-1/3 flex flex-col justify-center sm:justify-start text-center md:text-left"
        >
          <!-- prettier-ignore -->
          <svg width="37" height="37" fill="none" xmlns="http://www.w3.org/2000/svg" class="stroke-current text-gray-900 mb-4 mx-auto md:mx-0">
            <path
              d="M31.7429 20.6737L20.6892 31.7274c-.2864.2867-.6265.5141-1.0008.6693-.3743.1552-.7755.235-1.1807.235-.4052 0-.8064-.0798-1.1807-.235-.3743-.1552-.7144-.3826-1.0008-.6693L3.08333 18.4999V3.08325H18.5L31.7429 16.3262c.5743.5777.8966 1.3591.8966 2.1737 0 .8146-.3223 1.5961-.8966 2.1738zM10.7917 10.7917h.0141"
              stroke-width="3"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
          <h3 class="pb-4">Easily adoptable</h3>
          <p class="w-56 mx-auto md:mx-0">
            Neutral and clean style will play well with any UI.
          </p>
        </div>
      </div>
    </div>
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
