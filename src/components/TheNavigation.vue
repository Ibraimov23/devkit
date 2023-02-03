<template lang="pug">
nav
  div(class="xl:container py-10 justify-between items-center mx-auto px-4 flex")
    div(class="title font-bold text-2xl") DEV 
      span it
    ul(class="pa-0 flex" style="gap: 32px;")
      li(v-for="link in links" :key="link.href")
        a(
          :class="$route.path === link.href ? 'link-active' : null" 
          class="link font-semibold text-lg" 
          :href="link.href"
        ) {{ link.name }}
    a(class="font-semibold buy text-lg" href="#contacts")
      | Заказать 
</template>

<script>
export default {
  name: "TheNavigation",
  data: () => ({
    links: [
      {
        name: "Главная",
        href: "/",
      },
      {
        name: "Портфолио",
        href: "#portfolio",
      },
      {
        name: "Стоимость",
        href: "#stoimost",
      },
      {
        name: "Контакты",
        href: "#contacts",
      },
      {
        name: "О компании",
        href: "#about",
      },
    ],
  }),
};
</script>

<style scoped lang="scss">
.link {
  color: var(--base);
  transition: 0.2s ease-in-out color;
  position: relative;

  &:hover {
    color: #fff;
    transition: 0.2s ease-in-out color;
  }
}

.link-active {
  color: #fff;

  &::before {
    content: "";
    bottom: -5px;
    position: absolute;
    width: 88%;
    height: 2px;
    background-color: var(--primary-blue);
    left: 0;
  }
}

.title {
  position: relative;

  & > span {
    position: absolute;
    color: var(--primary-blue);
  }
}

.buy {
  width: 175px;
  height: 56px;
  border: solid 1px var(--primary-blue);
  border-radius: 16px;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}

@media screen and (max-width: 960px) {
  ul {
    display: none;
  }
}
</style>
