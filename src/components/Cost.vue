<template>
  <h2 class="cost">KOSZT: {{ sum }} zł</h2>
</template>
<script>
export default {
  data() {
    return {};
  },
  props: {
    ingredients: {
      type: Array,
    },
  },
  computed: {
    sum() {
      let cost = 0;
      this.ingredients.forEach((element) => {
        cost += element.value * element.price;
      });
      return cost.toFixed(2)
    },
  },
};
</script>
<style>
.cost {
  margin: auto;
  position: fixed;
 left: 50%;
  transform: translateX(-50%);
  top: 40%;
}
</style>