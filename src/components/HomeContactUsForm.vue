<template lang="pug">
div(class="card")
  v-form(ref="form" lazy-loading @submit.prevent="postForm")
    div(class="mb-3")
      div(class="pl-3 label font-semibold") Имя
      v-text-field(
        v-model="name"
        placeholder="Введите свое имя"
        solo
        class="input"
        hide-details
      )
    div(class="mb-3")
      div(class="pl-3 label font-semibold") Телефон
      v-text-field(
        v-model="phone"
        placeholder="Введите свой номер телефона"
        solo
        class="input"
        hide-details
      )
    div(class="mb-3")
      div(class="pl-3 label font-semibold") Мессенджер(необязательно)
      v-text-field(
        v-model="social"
        placeholder="Например телеграм"
        solo
        class="input"
        hide-details
      )
    div
      div(class="pl-3 label font-semibold") Email(необязательно)
      v-text-field(
        v-model="email"
        placeholder="Введите свой email"
        solo
        class="input"
        hide-details
      )
    button Заказать сайт
</template>

<script>
export default {
  name: "HomeContactUsForm",
  data: () => ({
    name: null,
    phone: null,
    social: null,
    email: null,
  }),
  methods: {
    postForm() {},
  },
};
</script>

<style scoped lang="scss">
.card {
  padding: 22px;
  width: 415px;
  padding-top: 27px;
  padding-bottom: 45px;
  background: #36414c;
  box-shadow: 5px 4px 70px rgba(14, 9, 66, 0.25);
  border-radius: 25px;
}

.label {
  margin-bottom: 12px;
  font-size: 20px;
}

button {
  width: 100%;
  font-weight: 600;
  font-size: 18px;
  background: #1e50ff;
  border-radius: 16px;
  height: 56px;
  margin-top: 44px;
}

@media screen and (max-width: 600px) {
  .card {
    width: 90vw;
  }

  .label {
    padding-left: 0 !important;
  }
}
</style>
