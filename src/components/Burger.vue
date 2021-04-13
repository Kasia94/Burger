<template>
    <div class="Burger">
    <div class="Burger__bread-top" />
    <div class="Burger__seeds " />
    <div class="Burger__meat"/>
    <div class="Burger__cheese"/>
    <div class="Burger__salad"/>
    <div class="Burger__becon"/>
    <div class="Burger__tomato"/>
    <div class="Burger__bread-bottom"/>
    </div>
</template>
 <style>
.Burger{
    border: solid pink 3px;
    height: 75vh;
    max-width: 100vh;
    top: 0;
}
.Burger__bread-bottom {
    height: 13%;
    width: 80%;
    background: linear-gradient(#F08E4A, #e27b36);
    border-radius: 0 0 30px 30px;
    box-shadow: inset -15px 0 #c15711;
    margin: 2% auto;
}
 .Burger__seeds {
    width: 7%;
    height: 8%;
    background-color: white;
    left: 44%;
    top: 0;
    border-radius: 40%;
    transform: rotate(10deg);
    box-shadow: inset -3px 0 #c9c9c9;
    position: relative;
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
    height: 8%;
    background: linear-gradient(#7f3608, #702e05);
    margin: 2% auto;
    border-radius: 15px;
}
.Burger__cheese {
    width: 90%;
    height: 4.5%;
    margin: 2% auto;
    background: linear-gradient(#f4d004, #d6bb22);
    border-radius: 20px;
}
.Burger__salad {
    width: 85%;
    height: 7%;
    margin: 2% auto;
    background: linear-gradient(#228c1d, #91ce50);
    border-radius: 20px;
}
.Burger__becon {
    width: 80%;
    height: 3%;
    background: linear-gradient(#bf3813, #c45e38);
    margin: 2% auto;
}
</style>