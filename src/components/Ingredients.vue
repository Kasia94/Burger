<template>
  <div class="Menu">
    <ul v-for="item in ingredients" :key="item.index">
      <li class="Menu__item">
        <p class="Menu__item-name">{{ item.name }}</p>
        <div class="Menu__item-value">
          <p>{{ item.value }} szt.</p>
          <div class="Menu__btns">
            <button @click="addIngredient(item.name)" class="Menu__btn-value">
              +
            </button>
            <button
              @click="removeIngredient(item.name)"
              class="Menu__btn-value"
            >
              -
            </button>
          </div>
        </div>
        <p class="price">{{ item.price }} zł</p>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  props: {
    ingredients: {
      type: Object,
    },
  },

  methods: {
    addIngredient(name) {
      const item = this.ingredients.find((i) => i.name === name);
      if (item.value >= 5) {
        return;
      }
      item.value++;
    },
    removeIngredient(name) {
      const item = this.ingredients.find((i) => i.name === name);
      if (item.value <= 0) {
        return;
      }
      item.value--;
    },
  },
};
</script>
<style lang="css">
.Menu {
  margin: auto;
  display: flex;
  flex-direction: column;
  background-color: rgb(235, 196, 149);
  width: 50%;
  min-width: 270px;
  border-radius: 10%;
}
.Menu__item {
  display: flex;
  flex-direction: row;
  height: 8vh;
  width: 100%;
  align-items: center;
  justify-content: space-around;
}
.Menu__item-name {
  display: inline-block;
  min-width: 60px;
  text-align: start;
}
.Menu__item-value {
  display: flex;
  height: 25px;
  padding-right: 40px;
  align-items: center;
}
.Menu__btns button {
  display: flex;
  flex-direction: column;
  padding: 8px;
  margin: 3px;
}
.Menu__btn-value {
  border-radius: 20%;
  height: 8px;
  width: 8px;
  align-items: center;
  justify-content: center;
}
</style>