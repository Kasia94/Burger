<template>
  <div class="Burger" :style="{ height: `${30 * sum}px`}">
    <div class="Burger__bread-top" />
    <template v-for="item in ingredients">
      <div v-for="element in item.value" :key="element.id" 
      :class="`Burger__${item.className}`"></div>
        <!-- <div class="Burger__meat"/>
    <div class="Burger__cheese"/>
    <div class="Burger__salad"/>
    <div class="Burger__becon"/>
    <div class="Burger__tomato"/> -->
    </template>
    <div class="Burger__bread-bottom" />
  </div>
</template>
<script>
export default {
  props: {
    ingredients: {
      type: Array,
    },
  },
  computed: {
    sum() {
      let valueElement = 0;
      this.ingredients.forEach((element) => {
        valueElement += element.value ;
      });
      return valueElement
    },
  },
};
</script>
 <style>
.Burger {
  /* height: 52vh; */
  width: 80vh;
  max-width: 100vh;
  margin: auto;
  margin-bottom: 2rem;
  margin-top: auto;
  position: relative;
}
.Burger__bread-bottom {
  height: 40px;
  width: 80%;
  background: linear-gradient(#f08e4a, #e27b36);
  border-radius: 0 0 30px 30px;
  box-shadow: inset -15px 0 #c15711;
  margin: 2% auto;
}
.Burger__seeds {
  display: inline-block;
  width: 7%;
  height: 8%;
  background-color: white;
  border-radius: 40%;
  transform: rotate(10deg);
  box-shadow: inset -3px 0 #c9c9c9;
  position: absolute;
  top: 90px
}

.Burger__bread-top {
  height: 20%;
  width: 80%;
  background: linear-gradient(#bc581e, #e27b36);
  border-radius: 50% 50% 0 0;
  box-shadow: inset -15px 0 #c15711;
  margin: 2% auto;
  position: relative;
  top: 15%;
}
.Burger__meat {
  width: 80%;
  height: 10px;
  background: linear-gradient(#7f3608, #702e05);
  margin: 2% auto;
  border-radius: 15px;
}
.Burger__cheese {
  width: 90%;
  height: 7px;
  margin: 2% auto;
  background: linear-gradient(#f4d004, #d6bb22);
  border-radius: 20px;
}
.Burger__salad {
  width: 85%;
  height: 5px;
  margin: 2% auto;
  background: linear-gradient(#228c1d, #91ce50);
  border-radius: 20px;
}
.Burger__becon {
  width: 80%;
  height: 8px;
  background: linear-gradient(#bf3813, #c45e38);
  margin: 2% auto;
}
.Burger__tomato {
  width: 80%;
  height: 8px;
  background: linear-gradient(#fa0909, #f06c6c);
  margin: 2% auto;
}
</style>