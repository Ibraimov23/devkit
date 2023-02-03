<template lang="pug">
section(class="home-steps" id="steps")
  div(class="xl:container container mx-auto px-4")
    div(class="blick")
    h2(class="title font-bold") Этапы Разработки
    div(class="steps flex justify-between flex-wrap")  
      div(class="step text-center px-7 py-7" v-for="step in steps" :key="step.id")
        div(class="textup") {{ step.title }}
        div(class="text font-bold") {{ step.subtitle }}
</template>

<script>
export default {
  name: "HomeSteps",
  data: () => ({
    steps: [
      {
        title: "№1 интервью",
        subtitle:
          "узнаем важную информацию о проекте, основных целях и задачах. проводим анализ ниши и UX-анализ.",
      },
      {
        title: "№2 структкра сайта",
        subtitle:
          "составляем структуру сайта на основе анализа и исследований каждый пункт согласовываем с заказчиком.",
      },
      {
        title: "№3 создание мудборда",
        subtitle:
          "составляем карту настроения сайта, показываем работы конкурентови определяемся со стилем дизайна.",
      },
      {
        title: "№4 прототип сайта",
        subtitle:
          "разрабатываем черновики вариант сайта на основе структуры, презентуем и согласовываем с заказчиком.",
      },
      {
        title: "№5 дизайн сайта",
        subtitle:
          "разрабатываем дизайн сайта на основе мудборда и прототипа, весь дизайн согласовываем с заказчиком.",
      },
      {
        title: "№6 верстка",
        subtitle:
          "переносним готовый дизайн в код, адаптируем сайт под все устройства и базовое SEO- продвижение.",
      },
      {
        title: "№7  хостинг+домен",
        subtitle:
          "загружаем сайт на платный хостинг, покупаем домен на основе пожеланий заказчика.",
      },
      {
        title: "№8 защита проекта",
        subtitle:
          "представляем сайт заказчику, обьясняем все рабочие моменты и причины выбора конкретных дизайн решений.",
      },
    ],
  }),
};
</script>

<style scoped lang="scss">
.title {
  font-size: 64px;
  line-height: 70px;
  margin-bottom: 100px;
}

.container {
  position: relative;
}

.blick {
  top: 546px;
  position: absolute;
  width: 644px;
  z-index: -1;
  height: 676px;
  left: 945px;
  background: rgba(30, 80, 255, 0.5);
  filter: blur(350px);
}

.textup {
  font-size: 24px;
  line-height: 32px;
}

.text {
  line-height: 32px;
}

.step {
  width: 380px;
  height: 230px;
  margin-bottom: 80px;
  background: #272d37;
  align-items: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 10px;
  border-radius: 25px;
}

.steps > *:last-child {
  margin-right: 37.5%;
}

@media screen and (max-width: 1680px) {
  .steps > *:last-child {
    margin-right: 34.5%;
  }
}

@media screen and (max-width: 1286px) {
  .step {
    margin-left: auto;
    margin-right: auto !important;
  }

  .blick {
    right: -50vw;
    left: initial;
  }
}

@media screen and (max-width: 600px) {
  .blick {
    right: -100vw;
  }
}
</style>
