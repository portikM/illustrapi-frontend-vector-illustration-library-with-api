<template>
  <button
    class="h-6 w-6 flex items-center justify-center bg-gray-200 rounded-full hover:bg-gray-400 focus:outline-none focus:bg-gray-400 cursor-pointer"
    v-on="$listeners"
  >
    <svg
      width="9"
      height="9"
      fill="none"
      class="text-gray-600 stroke-current"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path d="M.611.611l7.778 7.778M8.389.611L.611 8.389" />
    </svg>
  </button>
</template>
