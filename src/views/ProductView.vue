<template>
  <section class="products">
    <div class="container">
      <div class="products-header products-header--goods">
        <h2 class="products-header--title">Тануки</h2>
        <div class="products-header__info">
          <div class="products-header__rating">
            <img src="../assets/images/icons/star.svg" alt="star" />
            4.5
          </div>
          <div class="products-header__price">От 900 ₽</div>
          <div class="products-header__group">Пицца и суши</div>
        </div>
      </div>
      <div class="products-wrapper">
        <div class="products-card" v-for="good in store.goods" :key="good.id">
          <div class="products-card__image">
            <img :src="getUrl(good.image)" :alt="good.image" />
          </div>
          <div class="products-card__description">
            <div class="products-card__description-row">
              <h4 class="products-card__description--name">
                {{ good.title }}
              </h4>
            </div>
            <div class="products-card__description-row">
              <p class="products-card__description--text">
                {{ good.description }}
              </p>
            </div>
            <div class="products-card__description-row">
              <div class="products-card__description-controls">
                <button class="btn btn-primary">
                  В корзину
                  <img
                    src="../assets/images/icons/shopping-cart-white.svg"
                    alt="shopping-cart"
                  />
                </button>
                <span class="products-card__description-controls--price">
                  {{ good.price }} ₽
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { store } from "../store/index.js";

const getUrl = (name) =>
  new URL(`../assets/images/goods/${name}.jpg`, import.meta.url);
</script>
