<template>
  <div>
    <nav>
      <div class="max-w-6xl mx-auto py-4 px-2 sm:px-6 lg:px-8">
        <div class="relative flex items-center justify-between h-16">
          <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
            <button
              @click="menu = !menu"
              class="inline-flex items-center justify-center p-2 rounded-md text-gray-900 hover:bg-gray-200 focus:outline-none focus:bg-gray-200 transition duration-150 ease-in-out"
            >
              <svg
                fill="none"
                viewBox="0 0 24 24"
                class="stroke-current h-6 w-6"
              >
                <!-- prettier-ignore -->
                <path
                  :class="{ 'hidden': menu, 'inline-flex': !menu }"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h16"
                />
                <!-- prettier-ignore -->
                <path
                  :class="{ 'hidden': !menu, 'inline-flex': menu }"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M6 18L18 6M6 6l12 12"
                />
              </svg>
            </button>
          </div>
          <div
            class="flex-1 flex items-center justify-center sm:items-stretch sm:justify-start"
          >
            <a href="/" class="flex-shrink-0">
              <img
                class="block sm:hidden h-8 w-auto"
                :src="illustrapiMark"
                alt="illustrapi logo"
              />
              <img
                class="hidden sm:block h-8 w-auto"
                :src="illustrapiLogo"
                alt="illustrapi logo"
              />
            </a>
          </div>
          <div class="hidden sm:block sm:ml-6">
            <div class="flex">
              <a
                href="/browse"
                class="ml-4 px-3 py-2 rounded-md text-sm font-medium leading-5 font-bold text-gray-900 hover:bg-gray-200 focus:outline-none focus:bg-gray-200 transition duration-150 ease-in-out"
              >
                Browse
              </a>
              <!-- <a
                href="#"
                class="ml-4 px-3 py-2 rounded-md text-sm font-medium leading-5 font-bold text-gray-900 hover:bg-gray-200 focus:outline-none focus:bg-gray-200 transition duration-150 ease-in-out"
              >
                Pricing
              </a>
              <a
                href="#"
                class="ml-4 px-3 py-2 rounded-md text-sm font-medium leading-5 font-bold text-gray-900 hover:bg-gray-200 focus:outline-none focus:bg-gray-200 transition duration-150 ease-in-out"
              >
                Docs
              </a>
              <a
                href="#"
                class="ml-4 px-3 py-2 rounded-md text-sm font-medium leading-5 font-bold text-gray-900 hover:bg-gray-200 focus:outline-none focus:bg-gray-200 transition duration-150 ease-in-out"
              >
                Login
              </a> -->
            </div>
          </div>
          <div
            class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-4 sm:pr-0"
          >
            <!-- authenticated user nav -->
            <!-- <div v-if="authenticated" class="flex">
              <button
                class="p-1 border-2 border-transparent text-gray-900 rounded-full hover:bg-gray-200 focus:outline-none focus:bg-gray-200 transition duration-150 ease-in-out"
              >
                <svg
                  fill="none"
                  viewBox="0 0 24 24"
                  class="stroke-current h-6 w-6"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"
                  />
                </svg>
              </button>
              <ComDropdown>
                <button
                  slot="trigger"
                  class="flex text-sm border-2 border-transparent rounded-full sm:ml-3 focus:outline-none focus:border-teal-500 transition duration-150 ease-in-out"
                >
                  <img
                    class="h-8 w-8 rounded-full"
                    src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                    alt=""
                  />
                </button>
                <div slot="dropdown">
                  <a
                    href="#"
                    class="block px-4 py-2 text-sm leading-5 text-gray-600 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 transition duration-150 ease-in-out"
                  >
                    Your Profile
                  </a>
                  <a
                    href="#"
                    class="block px-4 py-2 text-sm leading-5 text-gray-600 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 transition duration-150 ease-in-out"
                  >
                    Your apps
                  </a>
                  <a
                    href="#"
                    class="block px-4 py-2 text-sm leading-5 text-gray-600 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 transition duration-150 ease-in-out"
                  >
                    Sign out
                  </a>
                </div>
              </ComDropdown>
            </div> -->
            <ComCta class="mr-2">Sign Up</ComCta>
          </div>
        </div>
      </div>
      <!-- prettier-ignore -->
      <div :class="{ 'block': menu, 'hidden': !menu }" class="sm:hidden">
        <div class="px-2 pt-2 pb-3">
          <a
            href="/browse"
            class="mt-1 block px-3 py-2 rounded-md text-base font-medium font-bold text-gray-900 hover:bg-gray-200 focus:outline-none focus:bg-gray-200 transition duration-150 ease-in-out"
          >
            Browse
          </a>
          <!-- <a
            href="#"
            class="mt-1 block px-3 py-2 rounded-md text-base font-medium font-bold text-gray-900 hover:bg-gray-200 focus:outline-none focus:bg-gray-200 transition duration-150 ease-in-out"
          >
            Pricing
          </a>
          <a
            href="#"
            class="mt-1 block px-3 py-2 rounded-md text-base font-medium font-bold text-gray-900 hover:bg-gray-200 focus:outline-none focus:bg-gray-200 transition duration-150 ease-in-out"
          >
            Docs
          </a>
          <a
            href="#"
            class="mt-1 block px-3 py-2 rounded-md text-base font-medium font-bold text-gray-900 hover:bg-gray-200 focus:outline-none focus:bg-gray-200 transition duration-150 ease-in-out"
          >
            Login
          </a> -->
        </div>
      </div>
    </nav>
    <main>
      <nuxt />
    </main>
  </div>
</template>

<script>
import illustrapiLogo from '~/assets/images/illustrapi.svg'
import illustrapiMark from '~/assets/images/illustrapi-mark.svg'

export default {
  data() {
    return {
      illustrapiMark,
      illustrapiLogo,
      menu: false,
      userNav: false
    }
  }
}
</script>

<style lang="scss">
@font-face {
  font-family: 'Muli';
  src: url('~assets/fonts/Muli/Muli-Regular.ttf');
  font-weight: normal;
}

@font-face {
  font-family: 'Muli';
  src: url('~assets/fonts/Muli/Muli-SemiBold.ttf');
  font-weight: 600;
}

@font-face {
  font-family: 'Muli';
  src: url('~assets/fonts/Muli/Muli-Bold.ttf');
  font-weight: bold;
}

@font-face {
  font-family: 'Muli';
  src: url('~assets/fonts/Muli/Muli-Black.ttf');
  font-weight: 900;
}

@font-face {
  font-family: 'Roboto-Mono';
  src: url('~assets/fonts/Roboto-Mono/RobotoMono-Regular.ttf');
  font-weight: normal;
}

html {
  font-family: 'Muli', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto,
    'Helvetica Neue', Arial, sans-serif;
  font-size: 1rem;
  word-spacing: 1px;
  @apply text-gray-600;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

// typorgaphy

.font-mono {
  font-family: 'Roboto-Mono';
}

h1,
h2 {
  @apply text-4xl text-gray-900 font-black text-center;
}

h3 {
  @apply text-xl text-gray-900 font-black;
}
</style>
