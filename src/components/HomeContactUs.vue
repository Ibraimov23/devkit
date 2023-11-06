<template lang="pug">
section(class="contact-us" id="contacts")
  div(class="xl:container container mx-auto px-4")
    h2(class="title text-center font-bold") Свяжитесь с  Нами 
    div(class="content flex flex-wrap")
      div
        div(class="subtitle font-medium") Заполните заявку, наш менеджер
          br
          | свяжется с вами в ближайшее время
        home-contact-us-form
      div
        div(class="subtitle font-medium") Или напишите сейчас в личные
          br
          | cообщения любой изданных соцсетей.
        div(class="socials")
          div(v-for="social in socials" :key="social.id")
            span(class="circle")
            | {{ social.type }}: {{ social.number }}
</template>

<script>
import HomeContactUsForm from "@/components/HomeContactUsForm";

export default {
  name: "HomeContactUs",
  components: { HomeContactUsForm },
  data: () => ({
    socials: [
      {
        type: "Телефон",
        number: "+996 551636369",
      },
      {
        type: "Telegram",
        number: "@ibraimov_nursultan",
      },
      {
        type: "Вконтакте",
        number: "@id510664514",
      },
      {
        type: "WhatsApp",
        number: "+996551636369",
      },
    ],
  }),
};
</script>

<style scoped lang="scss">
.contact-us {
  margin-top: 200px;
  padding-bottom: 204px;
}

.title {
  font-size: 64px;
  margin-bottom: 55px;
}

.content {
  & > * {
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    align-items: center;

    &:first-child {
      margin-bottom: 50px;
    }
  }
}

.socials {
  display: flex;
  flex-direction: column;
  gap: 21px;

  & > * {
    display: flex;
    align-items: center;
    gap: 18px;
    background: #d9d9d9;
    box-shadow: -4px 4px 25px rgba(30, 80, 255, 0.4);
    border-radius: 16px;
    width: 405px;
    padding-left: 24px;
    height: 60px;
    font-weight: 500;
    font-size: 20px;
    letter-spacing: 0.075em;
    text-transform: capitalize;
    color: #505050;
  }
}

.subtitle {
  font-size: 24px;
  margin-bottom: 50px;
}

.circle {
  width: 25px;
  height: 25px;
  display: block;
  border-radius: 50%;
  background: #1e50ff;
}

@media screen and (max-width: 600px) {
  .socials {
    & > * {
      width: 90vw !important;
      font-size: 16px !important;
    }
  }

  .subtitle {
    font-size: 20px;
  }
}
</style>
