<template lang="pug">
section(class="our-approach" id="about")
  div(class="xl:container flex container mx-auto px-4")
    div(class="left")
      h2(class="title mb-10 font-bold") Наш подход 
        br
        | к разработке
      div(class="subtitle font-semibold") Мы создаем уникальные сайты, основываясь 
        br
        | На пожеланиях клиента и современных
        br
        | Трендах Web-дизайна и маркетинга
        br
        br
        | В нашей команде опытные дизайнеры
        br
        | И разработчики, готовые воплотить любую
        br
        | Вашу идею в качественный сайт.
        br
        br
        | Мы заботимся о ваших проектах, ваших
        br
        | Сроках и ваших нервах, несмотря ни на что,
        br
        | И это-обещание.
    div(class="right flex items-center justify-center")
      img(class="mac" alt="mac" src="@/assets/img/mac.svg")
</template>

<script>
export default {
  name: "HomeOurApproach",
};
</script>

<style scoped lang="scss">
.our-approach {
  margin: 300px 0;
}

.title {
  font-size: 64px;
  line-height: 70px;
}

.subtitle {
  font-size: 18px;
  line-height: 32px;
}

.container {
  & > * {
    flex-grow: 1;
  }
}

@media screen and (max-width: 960px) {
  .title {
    font-size: 42px;
    line-height: 50px;
  }

  .subtitle {
    font-size: 16px;
    line-height: initial;
  }

  .mac {
    transform: scale(0.8);
  }
}

@media screen and (max-width: 600px) {
  .mac {
    position: absolute;
    left: 50%;
    margin-right: -50%;
    transform: translate(-15%, 0);
  }

  .container {
    padding: 0 !important;
  }

  .right {
    width: 100%;
    left: 0;
    overflow: hidden;
    position: absolute;
    height: 400px;
    z-index: -1;
  }

  .left {
    padding: 0 18px;
    background-color: rgba(255, 255, 255, 0);
    backdrop-filter: blur(16px);
    width: 100%;
  }
}
</style>
