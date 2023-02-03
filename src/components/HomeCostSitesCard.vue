<template lang="pug">
div(class="flex px-4 flex-wrap justify-center mx-auto container")
  div(class="card px-4 text-center" id="first")
    img(style="width: 80px; height: 80px;" class="mx-auto" src="@/assets/icons/icon-placeholder.svg" alt="icon")
    div(class="font-bold title capitalize") landing page
    div(class="subtitle") Одностраничный сайт, обычно
      br
      | направленный на презентаию
      br 
      | конкретного продукта или проекта
    div(class="price capitalize font-semibold") от 14000 ₽
  div(class="card px-4 text-center" id="two")
    img(style="width: 80px; height: 80px;" class="mx-auto" src="@/assets/icons/icon-placeholder.svg" alt="icon")
    div(class="font-bold title capitalize") многостраничник
    div(class="subtitle") Сайт, имеющий множество
      br 
      | дочерних страниц, подходи для
      br 
      | многих типов бизнеса 
    div(class="price capitalize font-semibold") от 26000 ₽
  div(class="card px-4 text-center" id="tree")
    img(style="width: 80px; height: 80px;" class="mx-auto" src="@/assets/icons/icon-placeholder.svg" alt="icon")
    div(class="font-bold title capitalize") инернет-магазин
    div(class="subtitle") Сайт, имеющий возможность
      br
      | покупки товаров онлайн
    div(class="price capitalize font-semibold") от 33000 ₽
</template>

<script>
export default {
  name: "HomeCostSitesCard",
};
</script>

<style scoped lang="scss">
.container {
  gap: 26px;
}

.title {
  font-size: 24px;
}

.card {
  background: #0c2144;
  display: flex;
  padding-top: 56px;
  padding-bottom: 26px;
  flex-direction: column;
  gap: 24px;
  border: 1px solid transparent;
  position: relative;
  border-radius: 16px;
  height: 368px;
  transition: 0.2s ease-in-out all;
  width: 384px;

  &:hover {
    transition: 0.2s ease-in-out all;
    background: #002b72;
    border: 1px solid;
    border-image-source: linear-gradient(
        136.6deg,
        #ffffff -14.02%,
        rgba(255, 255, 255, 0) 51.46%
      ),
      linear-gradient(317.85deg, #ffffff 0%, rgba(255, 255, 255, 0) 66.33%);
  }
}

.active {
  transition: 0.2s ease-in-out all;
  background: #002b72;
  border: 1px solid;
  border-image-source: linear-gradient(
      136.6deg,
      #ffffff -14.02%,
      rgba(255, 255, 255, 0) 51.46%
    ),
    linear-gradient(317.85deg, #ffffff 0%, rgba(255, 255, 255, 0) 66.33%);
}

.price {
  position: absolute;
  bottom: 26px;
  left: 50%;
  margin-right: -50%;
  transform: translate(-50%, 0);
  font-size: 18px;
}

.subtitle {
  color: var(--base);
  font-size: 14px;
}
</style>
