<script setup>
import Card from './components/Card.vue'
</script>

<template>
  <div class="card__title">Заголовок в app</div>
  <svg>
    <use href="./assets/sprite.svg#icon-fav"></use>
  </svg>
  <svg>
    <use href="./assets/sprite.svg#icon-lk"></use>
  </svg>
  <Card title="Рубашка 1" :price="30000 + 500" :is-added="true">
    <button>Добавить в корзину</button>
  </Card>
  <Card title="Рубашка 1" :price="30000 + 500" :is-added="true"> </Card>
  <Card title="Рубашка 1" :price="30000 + 500" :is-added="true"> </Card>
  <Card title="Рубашка 1" :price="30000 + 500" :is-added="true"> </Card>
</template>

<style>
body {
  background-color: #000;
  color: #fff;
}
</style>
