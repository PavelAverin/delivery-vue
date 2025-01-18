<template>
  <div
    class="cart-modal__overlay"
    :class="{ open: isOpen }"
    @click.self="closeModal()"
  >
    <div class="cart-modal">
      <div class="cart-modal__header">
        <h2 class="cart-modal__header--title">Корзина</h2>
        <span class="cart-modal__header--close" @click="closeModal()">
          <img src="../assets/images/icons/close.svg" alt="close" />
        </span>
      </div>

      <div class="cart-modal__body">
        <div class="cart-item">
          <p class="cart-item__title">Ролл угорь стандарт</p>

          <div class="cart-item__controls">
            <div class="cart-item__controls--price">250 ₽</div>
            <button class="btn btn-outline">-</button>
            <div class="cart-item__controls--count">1</div>
            <button class="btn btn-outline">+</button>
          </div>
        </div>

        <div class="cart-item">
          <p class="cart-item__title">Ролл угорь стандарт</p>

          <div class="cart-item__controls">
            <div class="cart-item__controls--price">250 ₽</div>
            <button class="btn btn-outline">-</button>
            <div class="cart-item__controls--count">1</div>
            <button class="btn btn-outline">+</button>
          </div>
        </div>

        <div class="cart-item">
          <p class="cart-item__title">Ролл угорь стандарт</p>

          <div class="cart-item__controls">
            <div class="cart-item__controls--price">250 ₽</div>
            <button class="btn btn-outline">-</button>
            <div class="cart-item__controls--count">1</div>
            <button class="btn btn-outline">+</button>
          </div>
        </div>

        <div class="cart-item">
          <p class="cart-item__title">Ролл угорь стандарт</p>

          <div class="cart-item__controls">
            <div class="cart-item__controls--price">250 ₽</div>
            <button class="btn btn-outline">-</button>
            <div class="cart-item__controls--count">1</div>
            <button class="btn btn-outline">+</button>
          </div>
        </div>

        <div class="cart-item">
          <p class="cart-item__title">Ролл угорь стандарт</p>

          <div class="cart-item__controls">
            <div class="cart-item__controls--price">250 ₽</div>
            <button class="btn btn-outline">-</button>
            <div class="cart-item__controls--count">1</div>
            <button class="btn btn-outline">+</button>
          </div>
        </div>
      </div>

      <div class="cart-modal__footer">
        <div class="cart-modal__footer--price">1250 ₽</div>
        <div class="cart-modal__footer--controls">
          <button class="btn btn-primary">Оформить заказ</button>
          <button class="btn btn-outline btn-cansel" @click="closeModal()">
            Отмена
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const { isOpen } = defineProps({ isOpen: Boolean });
const emit = defineEmits(["toggleModal"]);
const closeModal = () => emit("toggleModal");
</script>

<style scoped>
.cart-modal__overlay {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.4);
  align-items: center;
  justify-content: center;
}

.cart-modal__overlay.open {
  display: flex;
}

.cart-modal {
  width: 100%;
  max-width: 780px;
  padding: 40px 45px;
  border-radius: 5px;
  background-color: #fff;
}

.cart-modal__header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 45px;
}

.cart-modal__header--title {
  font-weight: 700;
  font-size: 36px;
  color: #000;
  margin: 0;
}
.cart-modal__header--close {
  cursor: pointer;
}

.cart-modal__body {
  margin-bottom: 50px;
}
.cart-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 10px;
}

.cart-item:not(:last-child) {
  padding-bottom: 10px;
  margin-bottom: 10px;
  border-bottom: 1px solid #d9d9d9;
}

.cart-item__title {
  font-weight: 400;
  font-size: 18px;
  line-height: 32px;
  color: #000;
  margin: 0;
}
.cart-item__controls {
  display: flex;
  align-items: center;
}

.cart-item__controls button {
  border: 1px solid #40a9ff;
  border-radius: 2px;
  padding: 5px 16px;
  font-weight: 400;
  font-size: 14px;
  line-height: 22px;
  text-align: center;
  color: #40a9ff;
}

.cart-item__controls--price {
  font-weight: 700;
  font-size: 20px;
  line-height: 32px;
  color: #000;
  margin-right: 45px;
}

.cart-item__controls--count {
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  text-align: center;
  color: #000;
  margin: 0 15px;
}

.cart-modal__footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 15px;
}

.cart-modal__footer--price {
  background-color: #262626;
  border-radius: 5px;
  padding: 15px 20px;
  font-weight: 700;
  font-size: 20px;
  color: #fafafa;
}

.cart-modal__footer--controls {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  column-gap: 10px;
}
</style>
