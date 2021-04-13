<template>
    <h2 class="cost">KOSZT: {{cost}} zł</h2>
</template>
<script>
export default {
   data(){
       return{
           cost:0
       }
   },
   props:{
       ingredients: {
      type: Object,
    },
   },
   methods:{},
   computed:{}
}
</script>
<style>
.cost{
   position: absolute;
   top: 80%;
   left:45%
}
</style>