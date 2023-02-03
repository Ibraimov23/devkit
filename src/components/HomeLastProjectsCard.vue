<template lang="pug">
div(class="without-props-block")
  div(class="card px-6 flex flex-wrap items-center")
    div
      div(class="mx-auto" style="width: fit-content;")
        h3(class="text-2xl mb-3 capitalize font-bold") приложение проигрыватель 
        div(class="font-bold mb-6 description") Приложение написано на JavaScript и фреймворке React. Также были использованы html и css.
        button(class="font-semibold") Смотреть полностью
    div
      div(class="mx-auto flex text-center justify-center items-center" style="width: fit-content;")
        img(class="image" src="@/assets/test/design.png" alt="first")
  div(class="card px-6 flex flex-wrap items-center")
    div
      div(class="mx-auto" style="width: fit-content;")
        h3(class="text-2xl mb-3 capitalize font-bold") таймер помодорро
        div(class="font-bold mb-6 description") Приложение написано на  чистом JavaScript. Также были использованы html и css.
        button(class="font-semibold") Смотреть полностью
    div
      div(class="mx-auto flex text-center justify-center items-center" style="width: fit-content;")
        img(class="image" src="@/assets/test/design.png" alt="first")
  div(class="card px-6 flex flex-wrap items-center")
    div
      div(class="mx-auto" style="width: fit-content;")
        h3(class="text-2xl mb-3 capitalize font-bold") таймер помодорро
        div(class="font-bold mb-6 description") Приложение написано на  чистом JavaScript. Также были использованы html и css.
        button(class="font-semibold") Смотреть полностью
    div
      div(class="mx-auto flex text-center justify-center items-center" style="width: fit-content;")
        img(class="image" src="@/assets/test/design.png" alt="first")
  div(class="card px-6 flex flex-wrap items-center")
    div
      div(class="mx-auto" style="width: fit-content;")
        h3(class="text-2xl mb-3 capitalize font-bold") таймер помодорро
        div(class="font-bold mb-6 description") Приложение написано на  чистом JavaScript. Также были использованы html и css.
        button(class="font-semibold") Смотреть полностью
    div
      div(class="mx-auto flex text-center justify-center items-center" style="width: fit-content;")
        img(class="image" src="@/assets/test/design.png" alt="first")
  div(v-if="!hover" class="card px-6 flex flex-wrap items-center")
    div
      div(class="mx-auto" style="width: fit-content;")
        h3(class="text-2xl mb-3 capitalize font-bold") таймер помодорро
        div(class="font-bold mb-6 description") Приложение написано на  чистом JavaScript. Также были использованы html и css.
        button(class="font-semibold") Смотреть полностью
    div
      div(class="mx-auto flex text-center justify-center items-center" style="width: fit-content;")
        img(class="image" src="@/assets/test/design.png" alt="first")
  div(v-if="!hover" class="card px-6 flex flex-wrap items-center")
    div
      div(class="mx-auto" style="width: fit-content;")
        h3(class="text-2xl mb-3 capitalize font-bold") таймер помодорро
        div(class="font-bold mb-6 description") Приложение написано на  чистом JavaScript. Также были использованы html и css.
        button(class="font-semibold") Смотреть полностью
    div
      div(class="mx-auto flex text-center justify-center items-center" style="width: fit-content;")
        img(class="image" src="@/assets/test/design.png" alt="first")
</template>

<script>
export default {
  name: "HomeLastProjectsCard",
  props: {
    project: Object,
    hover: Boolean,
  },
};
</script>

<style scoped lang="scss">
.card {
  background: #0f182e;
  border-radius: 24px;
  overflow: hidden;
  width: 100%;
  padding-top: 35px;
  padding-bottom: 18px;
  box-shadow: -5px 4px 50px rgba(0, 0, 0, 0.25) !important;
  gap: 24px;

  & > * {
    flex-grow: 1;
  }
}

.description {
  max-width: 335px;
}

button {
  width: 222px;
  height: 54px;
  font-size: 18px;
  border: 2px solid #1e50ff;
  border-radius: 16px;
}

.without-props-block {
  display: flex;
  gap: inherit;
  width: 100%;
  flex-direction: column;
}

.image {
  width: 300px;
  height: 158px;
  border-radius: 24px;
}
</style>
