<template lang="pug">
header
  div(class="xl:container container mx-auto px-4 flex")
    div(class="blick")
    div(class="blick2")
    div(class="flex-1 left flex justify-center flex-col")
      h1(class="font-bold mb-6") Закажите 
       br
       | Удобный сайт
       br
       | Под ключ
      div(class="text-xl subtitle") Разработаем качественный и быстрый
        br
        | сайт за короткие сироки, при заказе
        br
        | SEO-оптимизация в подарок!
      a(class="mt-10 font-semibold buy text-xl" href="#contacts")
        | Заказать сайт
    div(class="flex-1 right flex items-center justify-center")
      img(class="laptop" alt="laptop" src="@/assets/img/laptop.svg")
</template>

<script>
export default {
  name: "HomeHeader",
};
</script>

<style scoped lang="scss">
.subtitle {
  color: var(--base);
}

.container {
  height: inherit;
  position: relative;
}

.blick {
  width: 644px;
  height: 512px;
  left: -40vw;
  top: -474px;
  background: rgba(30, 80, 255, 0.75);
  filter: blur(350px);
  position: absolute;
  z-index: -1;
}

.blick2 {
  position: absolute;
  width: 644px;
  height: 676px;
  z-index: -1;
  right: -40vw;
  top: 246px;
  background: rgba(30, 80, 255, 0.5);
  filter: blur(350px);
}

header {
  height: 680px;
}

.buy {
  width: 300px;
  height: 56px;
  background-color: var(--primary-blue);
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 16px;
}

h1 {
  line-height: 80px;
  font-size: 65px;
}

@media screen and (min-width: 1580px) {
  .blick {
    left: -356px;
  }

  .blick2 {
    right: -148px;
  }
}

@media screen and (max-width: 960px) {
  h1 {
    line-height: initial;
    font-size: 42px;
  }

  .subtitle {
    font-size: initial;
  }
}

@media screen and (max-width: 600px) {
  .laptop {
    position: absolute;
    left: 50%;
    margin-right: -50%;
    transform: translate(-15%, 0);
  }

  .blick {
    left: -125%;
    top: -80%;
  }

  .blick2 {
    width: 575px;
    height: 380px;
    right: -101vw;
    top: 70%;
  }

  .container {
    padding: 0 !important;
  }

  .right {
    width: 100%;
    left: 0;
    overflow: hidden;
    position: absolute;
    height: inherit;
    z-index: -1;
  }

  .left {
    padding: 0 18px;
    width: 100%;
  }
}
</style>
