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
          <div class="flex-1 flex items-center justify-center sm:justify-start">
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
            <ComCtaLabel class="hidden sm:block ml-3">Coming soon</ComCtaLabel>
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
            <ComAnchor class="mr-2" href="/#sign-up">Sign Up</ComAnchor>
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
    <footer class="py-16 px-2 sm:px-6 lg:px-8 bg-gray-900">
      <div class="w-full max-w-6xl mx-auto flex flex-col sm:flex-row pb-10">
        <div
          class="w-full order-last sm:w-3/12 sm:pr-4 sm:order-first flex flex-col justify-center sm:block text-center sm:text-left pb-10 sm:pb-0"
        >
          <img
            class="h-8 w-auto mb-2"
            :src="illustrapiBw"
            alt="illustrapi logo"
          />
          <p class="text-sm">Copyright 2020, illustrapi.com</p>
        </div>
        <div
          class="w-full sm:w-1/5 flex flex-col items-center sm:items-baseline text-center sm:text-left pb-10 sm:pb-0"
        >
          <h4 class="mb-4">Illustrapi</h4>
          <a
            class="block text-white font-bold hover:text-gray-300 mb-2"
            href="/about"
          >
            About
          </a>
          <a
            class="block text-white font-bold hover:text-gray-300 mb-2"
            href="mailto:hello@illustrapi.com"
            target="_blank"
          >
            <span class="hidden lg:block">hello@illustrapi.com</span>
            <span class="lg:hidden">Contact</span>
          </a>
        </div>
        <div
          class="w-full sm:w-1/5 flex flex-col items-center sm:items-baseline text-center sm:text-left pb-10 sm:pb-0"
        >
          <h4 class="mb-4">Product</h4>
          <a
            class="block text-white font-bold hover:text-gray-300 mb-2"
            href="#"
          >
            Why illustrapi
          </a>
          <a
            class="block text-white font-bold hover:text-gray-300 mb-2"
            href="/browse"
          >
            Browse
          </a>
          <!-- <a
            class="block text-white font-bold hover:text-gray-300 mb-2"
            href="/pricing"
          >
            Pricing
          </a>
          <a
            class="block text-white font-bold hover:text-gray-300 mb-2"
            href="#"
          >
            Blog
          </a> -->
        </div>
        <div
          class="w-full sm:w-1/5 flex flex-col items-center sm:items-baseline text-center sm:text-left pb-10 sm:pb-0"
        >
          <!-- <h4 class="mb-4">API</h4>
          <a class="block text-white font-bold hover:text-gray-300" href="#">
            Docs
          </a>
          <a
            class="block text-white font-bold hover:text-gray-300"
            href="/browse"
          >
            Best practices
          </a> -->
        </div>
        <div
          class="w-full sm:w-1/6 flex justify-center sm:justify-end pb-10 sm:pb-0 items-baseline"
        >
          <!-- twitter -->
          <a class="block text-white hover:text-gray-300 p-1 mr-1" href="#">
            <!-- prettier-ignore -->
            <svg width="16" height="13" fill="none" xmlns="http://www.w3.org/2000/svg" class="fill-current">
              <path
                d="M16 1.54424c-.5884.25384-1.2287.43654-1.8882.50769.6847-.40685 1.1975-1.04962 1.4421-1.807691-.6426.382286-1.3465.650352-2.0805.792311-.3068-.32803-.6779-.58935-1.0901-.767682-.4122-.1783311-.8567-.2698522-1.3058-.26886002-1.81707 0-3.27844 1.47307202-3.27844 3.28077202 0 .25384.03077.50769.08076.75192C5.159 3.89039 2.73236 2.59039 1.1191.600008.825142 1.10215.671099 1.6739.672996 2.25578c0 1.13846.578774 2.1423 1.461364 2.73269C1.61424 4.96798 1.1063 4.825.651845 4.57116v.04038c0 1.59423 1.126785 2.91539 2.628535 3.21923-.28197.07325-.57204.11073-.86336.11154-.21344 0-.41534-.02115-.61916-.05.41534 1.3 1.62481 2.24419 3.06502 2.27499-1.12679.8827-2.53816 1.4019-4.070667 1.4019-.274967 0-.528783-.0096-.792213-.0404C1.45367 12.4615 3.17846 13 5.03593 13c6.03007 0 9.32967-4.99615 9.32967-9.33269 0-.1423 0-.28461-.0096-.42692.6384-.46731 1.1979-1.04615 1.644-1.69615z"
              />
            </svg>
          </a>

          <!-- medium -->
          <a class="block text-white hover:text-gray-300 p-1 mr-1" href="#">
            <!-- prettier-ignore -->
            <svg width="13" height="13" fill="none" xmlns="http://www.w3.org/2000/svg" class="fill-current">
              <path
                d="M12 0H.5C.223437 0 0 .223437 0 .5V12c0 .2766.223437.5.5.5H12c.2766 0 .5-.2234.5-.5V.5c0-.276563-.2234-.5-.5-.5zm-1.75 3.21406l-.6375.61094c-.05625.04219-.08281.11094-.07188.17813v4.49531c-.01093.06875.01563.1375.07188.17812l.625.61094v.13594H7.1v-.12969l.64531-.62656c.06407-.06406.06406-.08282.06406-.17813v-3.6375L6.0125 9.40781h-.24219L3.67969 4.85156v3.05469c-.01875.12813.02656.25781.11719.35l.84062 1.01719v.13594H2.25v-.13594l.84062-1.01719c.04429-.04575.07726-.10124.09625-.16201.01899-.06078.02349-.12516.01313-.18799V4.375c.01094-.09844-.02656-.19375-.10156-.26094l-.74688-.9v-.13594h2.32032L6.4625 7.00781l1.57656-3.92656H10.25v.13281z"
              />
            </svg>
          </a>

          <!-- dribbble -->
          <!-- <a class="block text-white hover:text-gray-300 p-1 mr-1" href="#"> -->
          <!-- prettier-ignore -->
          <!-- <svg
              width="13"
              height="13"
              viewBox="0 0 13 13"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
              class="fill-current"
            >
              <path
                d="M6.5 0C2.91563 0 0 2.91563 0 6.5C0 10.0844 2.91563 13 6.5 13C10.0844 13 13 10.0844 13 6.5C13 2.91563 10.0844 0 6.5 0ZM10.7984 2.99687C11.5719 3.94219 12.0406 5.14531 12.0516 6.45625C11.8687 6.41719 10.0328 6.04531 8.18594 6.27812C8.14688 6.18281 8.10781 6.0875 8.06719 5.99219C7.95156 5.72188 7.82812 5.45156 7.69844 5.1875C9.75 4.34844 10.6812 3.15625 10.7984 2.99687ZM6.5 0.95625C7.91094 0.95625 9.2 1.48594 10.1797 2.35469C10.0797 2.49688 9.24375 3.62031 7.27031 4.36094C6.36094 2.68906 5.35313 1.31719 5.19844 1.11094C5.625 1.00781 6.06094 0.95625 6.5 0.95625ZM4.13906 1.48438C4.28594 1.68438 5.27813 3.06094 6.19688 4.69531C3.6 5.38438 1.3125 5.375 1.06406 5.37187C1.425 3.64844 2.58594 2.21719 4.13906 1.48438ZM0.948437 6.50781C0.948437 6.45156 0.95 6.39375 0.951562 6.3375C1.19375 6.34219 3.88437 6.37656 6.65781 5.54688C6.81719 5.85781 6.96875 6.17344 7.10781 6.48906C7.03438 6.50937 6.96094 6.53125 6.88906 6.55469C4.025 7.48281 2.50156 10.0062 2.375 10.2203C1.48906 9.23594 0.948437 7.93437 0.948437 6.50781ZM6.5 12.0594C5.21562 12.0594 4.03281 11.6219 3.09219 10.8875C3.19219 10.6828 4.31562 8.5125 7.44687 7.42031L7.48281 7.40781C8.2625 9.43281 8.58438 11.1312 8.66719 11.6187C7.98228 11.9115 7.24484 12.0614 6.5 12.0594ZM9.60156 11.1109C9.54531 10.7734 9.25 9.14844 8.52344 7.15312C10.2641 6.875 11.7922 7.33125 11.9812 7.39062C11.7344 8.93437 10.8484 10.2687 9.60156 11.1109Z"
              />
            </svg>
          </a> -->

          <!-- product hunt -->
          <a class="block text-white hover:text-gray-300 p-1 mr-1" href="#">
            <!-- prettier-ignore -->
            <svg
              width="14"
              height="14"
              viewBox="0 0 14 14"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
              class="fill-current"
            >
              <path
                d="M8.98438 5.95312C8.98438 6.24479 8.88151 6.49219 8.67578 6.69531C8.47005 6.89844 8.22135 7 7.92969 7H5.95312V4.89844H7.92969C8.22135 4.89844 8.47005 5.0013 8.67578 5.20703C8.88151 5.41276 8.98438 5.66146 8.98438 5.95312ZM10.3828 5.95312C10.3828 5.27604 10.1445 4.69792 9.66797 4.21875C9.19141 3.73958 8.61198 3.5 7.92969 3.5H4.54688V10.5H5.95312V8.39844H7.92969C8.60677 8.39844 9.1849 8.16016 9.66406 7.68359C10.1432 7.20703 10.3828 6.63021 10.3828 5.95312ZM14 7C14 7.94792 13.8151 8.85417 13.4453 9.71875C13.0755 10.5833 12.5781 11.3281 11.9531 11.9531C11.3281 12.5781 10.5833 13.0755 9.71875 13.4453C8.85417 13.8151 7.94792 14 7 14C6.05208 14 5.14583 13.8151 4.28125 13.4453C3.41667 13.0755 2.67188 12.5781 2.04688 11.9531C1.42188 11.3281 0.924479 10.5833 0.554688 9.71875C0.184896 8.85417 0 7.94792 0 7C0 6.05208 0.184896 5.14583 0.554688 4.28125C0.924479 3.41667 1.42188 2.67188 2.04688 2.04688C2.67188 1.42188 3.41667 0.924479 4.28125 0.554688C5.14583 0.184896 6.05208 0 7 0C7.94792 0 8.85417 0.184896 9.71875 0.554688C10.5833 0.924479 11.3281 1.42188 11.9531 2.04688C12.5781 2.67188 13.0755 3.41667 13.4453 4.28125C13.8151 5.14583 14 6.05208 14 7Z"
              />
            </svg>
          </a>
        </div>
      </div>
      <!-- <div class="flex flex-col sm:flex-row justify-center text-center">
        <a
          class="block font-bold hover:text-gray-300 sm:mr-2"
          href="/privacy-policy"
        >
          Privacy policy
        </a>
        <span class="hidden sm:block mr-2">&#xb7;</span>
        <a class="block font-bold hover:text-gray-300 sm:mr-2" href="/terms">
          Terms
        </a>
        <span class="hidden sm:block mr-2">&#xb7;</span>
        <a
          class="block font-bold hover:text-gray-300"
          href="mailto:help@illustrapi.com"
          target="_blank"
        >
          Report a problem
        </a>
      </div> -->
    </footer>
  </div>
</template>

<script>
import illustrapiLogo from '~/assets/images/illustrapi.svg'
import illustrapiMark from '~/assets/images/illustrapi-mark.svg'
import illustrapiBw from '~/assets/images/illustrapi-bw.svg'

export default {
  data() {
    return {
      illustrapiMark,
      illustrapiLogo,
      menu: false,
      userNav: false,
      illustrapiBw
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
  scroll-behavior: smooth;
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

h4 {
  @apply font-bold;
}

// animations

.pop-up-enter-active,
.pop-up-leave-active {
  transition: all 0.5s;
}
.pop-up-enter,
.pop-up-leave-active {
  opacity: 0;
  transform: translateY(25px);
}
</style>
