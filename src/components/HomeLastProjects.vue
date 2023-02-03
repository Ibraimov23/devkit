<template lang="pug">
section(class="last-projects" id="portfolio")
  div(class="xl:container container mx-auto px-4")
    div(class="blick")
    h2(class="title text-center font-bold") Последние проекты
    div(class="flex" style="gap: 32px;")
      home-last-projects-card(:hover="hover")
    div(class="text-center")
      button(v-if="hover" class="capitalize font-semibold" @click="hover = false")
        | показать больше
</template>

<script>
import HomeLastProjectsCard from "./HomeLastProjectsCard";

export default {
  name: "HomeLastProjects",
  components: { HomeLastProjectsCard },
  data: () => ({
    hover: true,
  }),
};
</script>

<style scoped lang="scss">
.last-projects {
  padding: 130px 0;
}

.container {
  position: relative;
}

.blick {
  position: absolute;
  width: 638px;
  height: 552px;
  left: -324px;
  top: 960px;
  z-index: -1;
  background: rgba(30, 80, 255, 0.5);
  filter: blur(350px);
}

.title {
  font-size: 50px;
  margin-bottom: 55px;
}

button {
  margin-top: 76px;
  width: 216px;
  height: 54px;
  border: 2px solid #d5dde5;
  border-radius: 16px;
  font-size: 18px;
}

@media screen and (max-width: 600px) {
  .blick {
    bottom: 0;
    top: initial;
  }
}
</style>
