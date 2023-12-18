<script setup>
import Card from './components/Card.vue'
import Swiper from 'swiper'
import { Navigation } from 'swiper/modules'
// import Swiper and modules styles
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'

window.addEventListener('load', () => {
  var swiper = new Swiper('.mySwiper', {
    // Подключение нужных модулей
    modules: [Navigation],
    navigation: {
      nextEl: '.swiper-button-next',
      prevEl: '.swiper-button-prev'
    }
  })
})
</script>

<template>
  <div class="wrapper">
    <header class="header">
      <div class="container">
        <div class="header__row">
          <div class="header__logo logo">
            <div class="logo__image">
              <img src="./assets/logo.svg" alt="" />
            </div>
            <div class="logo__right">
              <div class="logo__name">REACT SNEAKERS</div>
              <div class="logo__desc">Магазин лучших кроссовок</div>
            </div>
          </div>
          <div class="header__menu menu">
            <nav class="menu__nav">
              <ul class="menu__list">
                <li class="menu__item">
                  <a href="" class="menu__link">
                    <svg class="menu__icon menu__icon--cart">
                      <use href="./assets/sprite.svg#icon-cart"></use>
                    </svg>
                    1205 руб.
                  </a>
                </li>
                <li class="menu__item">
                  <a href="" class="menu__link">
                    <svg class="menu__icon"><use href="./assets/sprite.svg#icon-fav"></use></svg>
                    Закладки
                  </a>
                </li>
                <li class="menu__item">
                  <a href="" class="menu__link">
                    <svg class="menu__icon"><use href="./assets/sprite.svg#icon-lk"></use></svg>
                    Профиль
                  </a>
                </li>
              </ul>
            </nav>
            <div class="element"></div>
          </div>
        </div>
      </div>
    </header>
    <main class="main">
      <div class="container">
        <!-- Swiper -->
        <div class="swiper mySwiper">
          <div class="swiper-wrapper">
            <div class="swiper-slide">
              <div class="banner-item">
                <div class="banner-item__row">
                  <div class="banner-item__content">
                    <div class="banner-item__logo"></div>
                    <div class="banner-item__name">
                      <span> Stan Smith,</span>
                      Forever!
                    </div>
                    <button class="banner-item__button"></button>
                  </div>
                  <img src="" alt="" class="banner-item__image" />
                </div>
              </div>
            </div>
          </div>
          <div class="swiper-button-next"></div>
          <div class="swiper-button-prev"></div>
        </div>
      </div>
    </main>
  </div>
</template>

<style>
body {
  background: #e7f6ff;
  padding-top: 85px;
}
.wrapper {
  max-width: 1080px;
  margin: 0 auto;
  border-radius: 20px;
  background: #fff;
  box-shadow: 0px 10px 20px 0px rgba(0, 0, 0, 0.04);
  min-height: 90vh;
}
.container {
  max-width: 960px;
  margin: 0 auto;
  width: 96%;
}

.header {
  padding: 44px 0;
  border-bottom: 1px solid #eaeaea;
}
.header__row {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.logo {
  display: flex;
  align-items: center;
}
.logo__image {
  flex-shrink: 0;
  margin-right: 16px;
  margin-left: -16px;
}
.logo__name {
  color: #000;
  font-size: 20px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  text-transform: uppercase;
}
.logo__desc {
  color: #9d9d9d;

  font-family: Inter;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

.menu__icon {
  height: 18px;
  width: 18px;
}
.menu__icon:not(.menu__icon--cart) {
  fill: #9b9b9b;
}
.menu__icon--cart {
  stroke: #9b9b9b;
}
.menu__list {
  display: flex;
  list-style: none;
  padding: 0;
  margin: 0;
}

.menu__link {
  display: flex;
  align-items: center;
  color: #5c5c5c;
  font-size: 14px;
  line-height: normal;
  text-decoration: none;
}
.menu__item + .menu__item {
  margin-left: 32px;
}
.menu__icon {
  flex-shrink: 0;
  margin-right: 8px;
}
</style>
