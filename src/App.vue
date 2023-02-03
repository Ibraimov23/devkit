<template lang="pug">
div(id="app")
  the-navigation 
  router-view
  the-footer
</template>

<script>
import TheNavigation from "@/components/TheNavigation";
import TheFooter from "@/components/TheFooter";

export default {
  components: { TheNavigation, TheFooter },
};
</script>

<style lang="scss">
#app {
  overflow: hidden;
}

:root {
  --black: #02050e;
  --base: #adb9c7;
  --primary-blue: #1e50ff;
}

html {
  scroll-behavior: smooth;
}

body {
  background-color: var(--black);
  font-family: "Poppins", sans-serif !important;
  color: #fff;
}

.v-input.input.v-input--hide-details.theme--light.v-text-field.v-text-field--single-line.v-text-field--solo.v-text-field--is-booted.v-text-field--enclosed.v-text-field--placeholder {
  border-radius: 16px;
  color: #505050;
  font-weight: 500;
  font-size: 20px;

  & > *:first-child {
    & > *:first-child {
      background: #d9d9d9;
      height: 60px;
      padding: 15px !important;
    }
  }
}

@media screen and (max-width: 600px) {
  h2 {
    line-height: 48px !important;
    font-size: 38px !important;
  }
}
</style>
