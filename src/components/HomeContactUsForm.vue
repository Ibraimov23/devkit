<template lang="pug">
div(class="card")
  v-form(ref="form" lazy-loading @submit.prevent="postForm")
    div(class="mb-3")
      div(class="pl-3 label font-semibold") Имя
      v-text-field(
        v-model="name"
        placeholder="Введите свое имя"
        solo
        required
        :rules="[(v) => !!v || 'Имя пользователя обязательно']"
        class="input"
        hide-details
      )
    div(class="mb-3")
      div(class="pl-3 label font-semibold") Телефон
      v-text-field(
        v-model="phone"
        placeholder="Введите свой номер телефона"
        solo
        :rules="phoneRules"
        required
        class="input"
        hide-details
      )
    div(class="mb-3")
      div(class="pl-3 label font-semibold") Мессенджер
      v-text-field(
        v-model="social"
        placeholder="Например телеграм"
        solo
        class="input"
        hide-details
      )
    div
      div(class="pl-3 label font-semibold") Email
      v-text-field(
        v-model="email"
        placeholder="Введите свой email"
        solo
        :rules="emailRules"
        class="input"
        hide-details
      )
    button(:disable="!valid" @click="postForm()") Заказать сайт
</template>

<script>
import axios from "axios";

export default {
  name: "HomeContactUsForm",
  data: () => ({
    name: null,
    phone: null,
    social: null,
    valid: false,
    email: null,
    phoneRules: null,
    emailRules: null,
  }),
  created() {
    const phone_regex = /\(?([0-9]{3})\)?([ .-]?)([0-9]{3})\2([0-9]{4})/;

    this.phoneRules = [
      (v) => !!v || "Номер телефона обязателен",
      (v) => phone_regex.test(v) || "Неверно введен номер телефона",
    ];

    this.emailRules = [
      (v) => !!v || "Email обязателен",
      (v) => /.+@.+\..+/.test(v) || "Не корректный email",
    ];
  },
  methods: {
    postForm() {
      if (this.$refs.form.validate()) {
        this.message = `<b>Заявка с сайта DEVit</b>\n\n`;
        this.message += `<b>Имя: </b><i>${this.name}</i>\n`;
        this.message += `<b>Номер телефона: </b><i>${this.phone}</i>\n`;
        this.message += `<b>Соц-сеть: </b><i>${this.social}</i>\n`;
        this.message += `<b>Email: </b><i>${this.email}</i>\n`;
        const api_url = `https://api.telegram.org/bot${this.$store.state.token}/sendMessage`;
        axios
          .post(api_url, {
            chat_id: this.$store.state.chat_id,
            parse_mode: "html",
            text: this.message,
          })
          .then(() => {
            this.email = null;
            this.phone = null;
            this.name = null;
            this.social = null;
          })
          .catch((errors) => {
            console.log(errors);
          });
      }
    },
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
