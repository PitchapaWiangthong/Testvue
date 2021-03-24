<template>
  <div id="Demo5">
      <img class="medium" v-bind:src="image" v-bind:height="height">
      <br>
      <a v-bind:href="link">My website</a>
      <br>
      <a :href="link">Myweb</a>
      <!-- :เป็นรูปย่อของbind -->
      <div :class="[false ? error : '', important]">CodeMobiles</div>
      <div :style="{color, fontSize}" :class="[important]">Bining Style</div>
      <div :style="isActive ? styleObj : '' " >Bining Style Obj</div>
      <button @click="isActive = !isActive">ToggerActive</button>
    
  </div>
</template>

<script>
export default {
name:"Demo5",
data() {
    return {
        image:"https://www.flaticon.com/svg/vstatic/svg/1828/1828925.svg?token=exp=1616589652~hmac=9c1d50f9de54f3eba5eb9e12f85e3835",
        height: 150,
        link: "http://www.google.com",
        error: "error_class",
        important:"important",
        color: "green",
        fontSize: "30px",
        styleObj: {
            backgroundColor: 'yellow',
            color: 'white'
        },
        isActive:false
    }
},
}
</script>

<style>
    .error_class{
        background-color: brown;
        color: white;
    }
    .important{
        /* ทำตัวหนา */
        font-weight: 900;
    }
</style>