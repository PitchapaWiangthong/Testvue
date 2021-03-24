<template>
  <div app ="Demo2">
      <h1>Event and Method</h1>
      <!-- คลิ้กแล้วเด้งข้อความ -->
      <button v-on:click="clickme">ClickMe</button>
      <button v-on:click="clickme2('Welcome to myweb')">ClickMe2</button>
      <button @click="clickme2('Perth')">ClickMe3</button>
      <h3 class="content">{{getTime()}}</h3>
  </div>
</template>

<script>
export default {
    name:"Demo2",
    methods: {
        clickme(){
            alert("HI")
        },
        clickme2(message){
            alert(message)
        },
        getTime(){
            return Date();
        }

    },
}
</script>

<style>

</style>