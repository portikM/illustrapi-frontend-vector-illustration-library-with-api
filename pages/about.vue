<template>
  <div class="flex flex-col justify-center max-w-5xl mx-auto px-4 pt-16">
    <section class="max-w-3xl mx-auto text-lg pb-16">
      <h1 class="pb-10">
        Thde idea
      </h1>
      <div class="pb-10">
        <p>
          We came up with the idea to create an illustration library with an API
          after we couldn’t find one we could to use for our project. While there
          were a lot of really beautiful and free open-source vector image
          libraries like <a class="border-b hover:text-gray-400" href="https://undraw.co/" target="_blank">unDraw</a>, <a
            class="border-b hover:text-gray-400"
            href="https://www.humaaans.com/"
            target="_blank"
          >humaaans</a> and <a
            class="border-b hover:text-gray-400"
            href="https://isometric.online/"
            target="_blank"
          >isometric</a>, none of
          them had
          an API. We were searching for a design toolkit which would allow us to
          implement user search through the library or dynamically render
          illustrations, but surprisingly couldn't find neither free nor paid
          services of that kind. We couldn’t miss on a chance to become the <span class="font-bold text-teal-500">first
            one of a kind</span>, so we decided to create our own.
        </p>
        <br />
        <p>
          We are passionate about things we do, which is why we intended
          illustrapi to be a tool you could use to improve your user experience.
          As for the concept in illustrations, here are some of the things we
          value:
        </p>
        <ul class="list-inside list-disc pt-2">
          <li>Diversity allows everyone to feel included</li>
          <li>Simplicity conveys sophistication</li>
          <li>Detalization communicates thofullness</li>
        </ul>

        <br />
        <p>
          Another big aspect we kept in mind while creating illustrapi is open source community.
          While illustrapi is not going to be free and open source for everyone,
          we will allow using our solution <span class="font-bold text-teal-500">free of charge for personal and open
            source non-commercial projects.</span>
        </p>
      </div>
      <div class="pb-10">
        <h1 class="pb-10">
          Team
        </h1>
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-10">
          <!-- Maksym Portianoi -->
          <div class="w-fill bg-gray-100 rounded-lg shadow-lg text-center">
            <div class="w-full p-6 flex flex-col items-center justify-center rounded-t-lg border-t-8 border-teal-500">
              <img class="rounded-full w-48 mb-6" :src="maxPhoto" alt="Maksym Portianoi" />
              <h3>
                Maksym Portianoi
              </h3>
              <h4 class="text-gray-500 pb-2">
                Creator, Designer &amp; Developer
              </h4>
              <p class="pb-4">
                I am software developer passionate about the tech world. But secretly I dream of becoming a rock star. You might even catch me playing imaginary drums as I work with my headphones on. I am hoping to play in my own band one day.
              </p>
              <div class="flex justify-center">
                <!-- twitter -->
                <a class="block text-gray-600 hover:text-gray-500 p-1 mr-1" target="_blank" href="https://twitter.com/portik_m">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="13"
                    height="13"
                    viewBox="0 0 22 22"
                    fill="none"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    class="stroke-current"
                  >
                    <path d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z" />
                  </svg>
                </a>
                <!-- dribbble -->
                <a class="block text-gray-600 hover:text-gray-500 p-1 mr-1" target="_blank" href="https://dribbble.com/portik">
                  <!-- prettier-ignore -->
                  <svg
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
                </a>
                <!-- github -->
                <a class="block text-gray-600 hover:text-gray-500 p-1 mr-1" target="_blank" href="https://github.com/portikM">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="13"
                    height="13"
                    viewBox="0 0 22 22"
                    fill="none"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    class="stroke-current"
                  >
                    <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 00-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0020 4.77 5.07 5.07 0 0019.91 1S18.73.65 16 2.48a13.38 13.38 0 00-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 005 4.77a5.44 5.44 0 00-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 009 18.13V22" />
                  </svg>
                </a>
              </div>
            </div>
          </div>

          <!-- Anna Kovner -->
          <div class="w-fill bg-gray-100 rounded-lg shadow-lg text-center">
            <div class="w-full p-6 flex flex-col items-center justify-center rounded-t-lg border-t-8 border-teal-500">
              <img class="rounded-full w-48 mb-6" :src="annaPhoto" alt="Maksym Portianoi" />
              <h3>
                Anna Kovner
              </h3>
              <h4 class="text-gray-500 pb-2">
                Illustrator
              </h4>
              <p class="pb-4">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
              </p>
              <div class="flex justify-center">
                <!-- facebook -->
                <a class="block text-gray-600 hover:text-gray-500 p-1 mr-1" target="_blank" href="#">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="13"
                    height="13"
                    viewBox="0 0 22 22"
                    fill="none"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    class="stroke-current"
                  >
                    <path d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z" />
                  </svg>
                </a>
                <!-- behance -->
                <a class="block text-gray-600 hover:text-gray-500 p-1 mr-1" target="_blank" href="#">
                  <svg
                    width="20"
                    height="13"
                    viewBox="0 0 20 13"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                    class="fill-current"
                  >
                    <path d="M7.36588 4.92632C7.52054 4.83509 7.63654 4.70476 7.71387 4.53534C7.7912 4.36591 7.82987 4.15739 7.82987 3.90977C7.82987 3.37544 7.62365 3.02356 7.21121 2.85414C6.86322 2.73684 6.425 2.6782 5.89657 2.6782H2.93862V5.2H6.16723C6.657 5.2 7.05655 5.10877 7.36588 4.92632ZM7.03722 3.90977C7.03722 4.09223 7.01144 4.20301 6.95988 4.24211C6.77944 4.3594 6.51522 4.41805 6.16723 4.41805H3.73127V3.46015H5.89657C6.32189 3.46015 6.66989 3.50576 6.94055 3.59699L6.95022 3.60677L6.97922 3.63609L7.00822 3.68496L7.02755 3.77293L7.03722 3.90977ZM7.32721 7.19399C7.28854 7.16792 7.24343 7.14837 7.19188 7.13534C7.14033 7.12231 7.08555 7.10602 7.02755 7.08647C6.96955 7.06692 6.90833 7.05388 6.84389 7.04737L6.65056 7.02782L6.43789 7.00827L6.2059 6.9985H2.93862V10.0481H6.16723C6.41212 10.0481 6.628 10.0318 6.81489 9.99925C7.00177 9.96667 7.1661 9.91779 7.30788 9.85263C7.79765 9.60501 8.04253 9.12932 8.04253 8.42556C8.04253 8.12581 7.98453 7.87168 7.86854 7.66316C7.75254 7.45464 7.5721 7.29825 7.32721 7.19399ZM3.73127 7.78045H6.2059C6.41212 7.79348 6.57967 7.80977 6.70855 7.82932C6.83744 7.84887 6.93411 7.8782 6.99855 7.91729C7.17899 7.99549 7.26921 8.16491 7.26921 8.42556C7.26921 8.79048 7.1661 9.02506 6.95988 9.12932C6.947 9.14236 6.93088 9.15213 6.91155 9.15865C6.89222 9.16516 6.86644 9.17168 6.83422 9.1782C6.802 9.18471 6.76333 9.19449 6.71822 9.20752C6.67311 9.22055 6.62478 9.23033 6.57322 9.23684C6.52167 9.24336 6.46045 9.24662 6.38956 9.24662H3.73127V7.78045ZM16.4717 5.66917C16.3557 5.56491 16.2301 5.4802 16.0947 5.41504C15.9594 5.34987 15.8176 5.301 15.6694 5.26842C15.5212 5.23584 15.3633 5.21955 15.1957 5.21955C14.9122 5.21955 14.6609 5.25865 14.4418 5.33684C14.2227 5.41504 14.0358 5.53233 13.8811 5.68872C13.5718 6.01454 13.3784 6.45113 13.3011 6.9985V7.03759H17.071L17.0517 6.9985C17.0002 6.41203 16.8068 5.96892 16.4717 5.66917ZM14.4611 6.23609C14.6158 6.0797 14.8606 6.0015 15.1957 6.0015C15.4922 6.0015 15.7371 6.0797 15.9304 6.23609H14.4611ZM19.9323 6.66617C19.8163 5.91028 19.5586 5.23258 19.159 4.63308C19.0301 4.45063 18.8948 4.2812 18.753 4.12481C18.6112 3.96842 18.4598 3.82506 18.2987 3.69474C18.1376 3.56441 17.9668 3.44712 17.7864 3.34286V0.195489H12.5858V3.36241C12.2765 3.55789 11.9865 3.79248 11.7158 4.06617C11.11 4.6787 10.7105 5.47368 10.5172 6.45113C10.4398 6.34687 10.3593 6.24586 10.2755 6.14812C10.1917 6.05038 10.0983 5.95589 9.99517 5.86466C10.0081 5.85163 10.0209 5.84185 10.0338 5.83534C10.0467 5.82882 10.0596 5.81253 10.0725 5.78647C10.5236 5.2391 10.7492 4.52882 10.7492 3.65564C10.7492 2.83459 10.5365 2.11779 10.1112 1.50526C9.40229 0.52782 8.24875 0.0260652 6.65056 0H0V12.7263H6.2639C6.88255 12.7263 7.4561 12.6677 7.98453 12.5504C8.28097 12.4852 8.55808 12.394 8.81585 12.2767C9.07363 12.1594 9.31207 12.016 9.53117 11.8466C9.7245 11.7033 9.90172 11.5404 10.0628 11.3579C10.2239 11.1754 10.3689 10.9734 10.4978 10.7519C10.6009 10.5825 10.6912 10.413 10.7685 10.2436C10.8974 10.5694 11.0553 10.8627 11.2421 11.1233C11.429 11.384 11.6449 11.612 11.8898 11.8075C12.8693 12.6025 13.9907 13 15.2537 13C16.8004 13 18.0119 12.5113 18.8884 11.5338C19.4683 10.9213 19.797 10.2827 19.8743 9.61805L19.9323 9.18797H19.9903V8.42556C20.0032 8.06065 20.0032 7.73158 19.9903 7.43835C19.9774 7.14511 19.9581 6.88772 19.9323 6.66617ZM8.62252 5.92331L8.56452 5.94286L8.64186 5.98195C9.19607 6.17744 9.61495 6.5 9.8985 6.94962C10.1821 7.39925 10.3238 7.94336 10.3238 8.58196C10.3238 8.79048 10.3077 8.999 10.2755 9.20752C10.2433 9.41604 10.1885 9.61479 10.1112 9.80376C10.0338 9.99273 9.94361 10.1719 9.8405 10.3414C9.63428 10.6932 9.37651 10.9865 9.06718 11.2211C8.71919 11.4947 8.30675 11.6837 7.82987 11.788C7.35299 11.8792 6.831 11.9248 6.2639 11.9248H0.792653V0.781955H6.63122C7.97164 0.80802 8.91896 1.20551 9.47318 1.97444L9.62784 2.20902L9.7535 2.46316L9.85017 2.74662L9.9275 3.03985L9.96617 3.34286L9.97583 3.65564C9.97583 4.33333 9.80828 4.8807 9.47318 5.29774C9.27985 5.5193 8.99629 5.72782 8.62252 5.92331ZM15.1957 2.69774C14.9766 2.69774 14.7833 2.70426 14.6158 2.71729H13.3784V0.977444H17.013V2.71729H15.7757C15.5437 2.70426 15.3504 2.69774 15.1957 2.69774ZM13.2624 8.42556C13.2624 8.63409 13.285 8.82957 13.3301 9.01203C13.3752 9.19449 13.4332 9.36065 13.5041 9.51053C13.575 9.6604 13.662 9.79073 13.7651 9.9015C13.8682 10.0123 13.9907 10.1133 14.1324 10.2045C14.4675 10.413 14.8671 10.5173 15.3311 10.5173C15.4471 10.5173 15.5631 10.5108 15.6791 10.4977C15.7951 10.4847 15.9014 10.4619 15.9981 10.4293C16.0947 10.3967 16.1882 10.3544 16.2784 10.3023C16.3686 10.2501 16.4524 10.1915 16.5297 10.1263C16.5813 10.0872 16.6328 10.0383 16.6844 9.9797C16.7359 9.92105 16.7875 9.85915 16.8391 9.79399C16.8906 9.72882 16.9357 9.65063 16.9744 9.5594H19.101C19.0366 10.0416 18.7788 10.5238 18.3277 11.006C17.593 11.814 16.5684 12.218 15.2537 12.218C15.0991 12.218 14.9476 12.2115 14.7994 12.1985C14.6512 12.1855 14.5062 12.1627 14.3644 12.1301C14.2227 12.0975 14.0809 12.0617 13.9391 12.0226C13.7973 11.9835 13.6588 11.9378 13.5234 11.8857C13.3881 11.8336 13.256 11.7717 13.1271 11.7C12.9982 11.6283 12.8726 11.5501 12.7501 11.4654C12.6277 11.3807 12.5085 11.2927 12.3925 11.2015C11.5676 10.5238 11.1551 9.42256 11.1551 7.89774C11.1551 6.47719 11.5289 5.38897 12.2765 4.63308C12.908 3.98145 13.7007 3.60351 14.6544 3.49925H15.7177C15.9755 3.52531 16.2172 3.57093 16.4427 3.63609C16.6683 3.70125 16.8842 3.77945 17.0904 3.87068C17.3739 4.001 17.6349 4.16717 17.8734 4.36917C18.1118 4.57118 18.3212 4.80902 18.5017 5.08271C18.8368 5.56491 19.0495 6.13183 19.1397 6.78346C19.2041 7.1614 19.2299 7.70226 19.217 8.40602H13.2624V8.42556ZM16.0464 9.5203C15.8788 9.66366 15.6404 9.73534 15.3311 9.73534C15.2151 9.73534 15.112 9.72556 15.0217 9.70602C14.9315 9.68647 14.8478 9.66366 14.7704 9.63759C14.6931 9.61153 14.6158 9.57895 14.5384 9.53985C14.3966 9.43559 14.2871 9.3183 14.2098 9.18797H16.2784C16.2011 9.33133 16.1237 9.44211 16.0464 9.5203Z" />
                  </svg>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="pb-10">
        <h1 class="pb-10">
          FAQs
        </h1>
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-10">
          <div>
            <h3 class="pb-2">
              When is it gonna be available?
            </h3>
            <p>
              We don’t have any timeframes yet. Right now we are in very early development stages and drawing illustrations. You can <router-link class="border-b hover:text-gray-400" :to="{ path: '/#sign-up' }" target="_blank">sign up</router-link> for project updates, early previews and to find out when it’s ready.
            </p>
          </div>
          <div>
            <h3 class="pb-2">
              Is it gonna be free?
            </h3>
            <p>
              No. While illustrapi is not going to be free and open source for everyone, we will allow using our solution <span class="font-bold text-teal-500">free of charge for personal and open
                source non-commercial projects.</span>
            </p>
          </div>
          <div>
            <h3 class="pb-2">
              How much will it cost?
            </h3>
            <p>
              We will release pricing plans when we announce an official release.
            </p>
          </div>
          <div>
            <h3 class="pb-2">
              I want to use it ASAP
            </h3>
            <p>
              You can help us by telling us about your project so we could address your needs. Please <router-link class="border-b hover:text-gray-400" :to="{ path: '/#sign-up' }" target="_blank">sign up</router-link> for our newsletter and we will contact you to hear more.
            </p>
          </div>
          <div>
            <h3 class="pb-2">
              I can draw. Can I help?
            </h3>
            <p>
              Yes! Please contact us at <a class="border-b hover:text-gray-400" href="mailto:hello@illustrapi.com" target="_blank">hello@illustrapi.com</a> if you want to contribute.
            </p>
          </div>
          <div>
            <h3 class="pb-2">
              I can code. Can I help?
            </h3>
            <p>
              Absolutely. Shoot us an email at <a class="border-b hover:text-gray-400" href="mailto:hello@illustrapi.com" target="_blank">hello@illustrapi.com</a> if you wish to be a part of this.
            </p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import maxPhoto from '~/assets/images/team/max.jpg'
import annaPhoto from '~/assets/images/team/anna.jpg'

export default {
  data() {
    return {
      maxPhoto,
      annaPhoto
    }
  }
}
</script>
