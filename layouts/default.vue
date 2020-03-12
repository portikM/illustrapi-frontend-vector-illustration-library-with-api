<template>
  <div>
    <nuxt />
  </div>
</template>

<style lang="scss">
@font-face {
  font-family: "Muli";
  src: url("~assets/fonts/Muli/Muli-Regular.ttf");
  font-weight: normal;
}

@font-face {
  font-family: "Muli";
  src: url("~assets/fonts/Muli/Muli-SemiBold.ttf");
  font-weight: 600;
}

@font-face {
  font-family: "Muli";
  src: url("~assets/fonts/Muli/Muli-Bold.ttf");
  font-weight: bold;
}

@font-face {
  font-family: "Muli";
  src: url("~assets/fonts/Muli/Muli-Black.ttf");
  font-weight: 900;
}

@font-face {
  font-family: "Roboto-Mono";
  src: url("~assets/fonts/Roboto-Mono/RobotoMono-Regular.ttf");
  font-weight: normal;
}

html {
  font-family: "Muli", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
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
</style>
