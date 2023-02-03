<template lang="pug">
footer(class="footer" id="footer")
  div(class="xl:container container mx-auto px-4 flex")
    div 
      div(class="title font-bold mb-4 text-2xl") DEV 
        span it
      div Мы заботимся о ваших
        br
        | проектах, сроках, нервах,
        br
        | несмотря ни на что.
      div(class="mt-11") 2022 All Right Reserved
    div(class="right")
      div
        a(href="#") Главная
        a(href="#") Заказать
        a(href="#") Контакты
      div
        a(href="#") Стоимость 
        a(href="#") Портфолио
      div(class="media")
        div(class="text-center") Россия 2022  
        div(class="socials")
          a(href="#")
            img(class="icon" alt="telegram" src="@/assets/icons/telegram-icon.svg")
          a(href="#")
            img(class="icon" alt="whatsapp" src="@/assets/icons/whatsapp-icon.svg")
          a(href="#")
            img(class="icon" alt="vkontakte" src="@/assets/icons/vkontakte-icon.svg")
    div(class="blick")
</template>

<script>
export default {
  name: "TheFooter",
};
</script>

<style scoped lang="scss">
.footer {
  overflow: hidden;
  padding-top: 50px;
  padding-bottom: 100px;
}

.title {
  position: relative;

  & > span {
    position: absolute;
    color: var(--primary-blue);
  }
}

.icon {
  width: 100%;
  height: 100%;
}

.media {
  gap: 0px !important;
}

.blick {
  position: absolute;
  width: 638px;
  height: 392px;
  left: -416px;
  bottom: -320px;
  background: rgba(30, 80, 255, 0.5);
  filter: blur(350px);
}

.container {
  display: flex;
  flex-wrap: wrap;
  position: relative;

  & > * {
    flex-grow: 1;

    &:first-child {
      margin-bottom: 50px;

      & > *:nth-child(2) {
        color: #adb9c7;
        line-height: 32px;
      }

      & > *:last-child {
        font-size: 14px;
        line-height: 24px;
      }
    }
  }
}

.socials {
  display: flex;
  align-items: center;
  justify-content: center;

  & > * {
    overflow: hidden;
    width: 66px;
    display: block;
    height: 66px;
  }
}

.right {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;

  & > * {
    flex-grow: inherit;
    display: flex;
    gap: 12px;
    color: #adb9c7;
    flex-direction: column;

    & > * {
      transition: 0.2s ease-in-out color;

      &:hover {
        color: #fff;
        transition: 0.2s ease-in-out color;
      }
    }
  }
}

@media screen and (max-width: 600px) {
  .footer {
    padding-bottom: 50px;
  }
}
</style>
