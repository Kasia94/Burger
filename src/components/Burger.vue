<template>
  <div class="Burger" :style="{ height: `${20 * sum}px`}">
    <div class="Burger__bread-top">
      <div class="Burger__seeds"></div>
      <div class="Burger__seeds"></div>
      <div class="Burger__seeds"></div>
    </div>
    <template v-for="item in ingredients">
      <div v-for="element in item.value" :key="element.id" 
      :class="`Burger__${item.className}`"></div>
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
  width: 80vh;
  max-width: 100vh;
  margin: auto;
  margin-bottom: 300px;
  margin-top: auto;
  position: relative;
}
.Burger__bread-bottom {
  height: 20px;
  width: 80%;
  background: linear-gradient(#f08e4a, #e27b36);
  border-radius: 0 0 30px 30px;
  box-shadow: inset -15px 0 #c15711;
  margin: 2% auto;
}
.Burger__seeds {
  display: inline-block;
  width: 15%;
  height: 20%;
  background-color: white;
  border-radius: 40%;
  transform: rotate(10deg);
  box-shadow: inset -3px 0 #c9c9c9;
   z-index: 2;
  /* margin-top: 10px;
  transform:  translateY(-30px); */
}

.Burger__bread-top {
  height: 20px;
  width: 80%;
  background: linear-gradient(#bc581e, #e27b36);
  border-radius: 50% 50% 0 0;
  box-shadow: inset -15px 0 #c15711;
  margin: 2% auto;
  position: relative;
  margin-bottom: 2px;
  
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