<template>
  <div>
      <h1>Data</h1>
      <!-- คลิ้กแล้วสามารถเพิ่มค่าของดาต้า -->
      <button @click="count++; isLogged=true;">Count++</button>
      <span>{{count}}</span>
      <div>{{message}}</div>
      <input type="text" placeholder="Enter a message" v-model="message">
      <!-- ถ้า isLogged เป็น true woww! จะแสดง -->
      <h2 v-if="isLogged">Woww!</h2>
      <!-- แสดงข้อความarray -->
      <div>{{account}} {{account.username}} {{account.password}} </div>
      <div>{{courses}}</div>
      <div>{{courses[3]}}</div>
      <ul>
          <li v-for ="(item, index) in courses" :key="index">{{index+1}}. {{item}}</li>
      </ul>
      <span class="title">Oppa</span>


  </div>
</template>

<script>
export default {
    name:"Demo3",
    mounted() {
    this.messaage = "Welcome to mywebsite"
    },
    data() {
        return {
            count: 0,
            messaage: "",
            isLogged: false,
            account:{
                username:"admin",
                password:1234
            },
            courses:[
                "Angular",
                "VueJS",
                "React",
                "Fluter"
            ]
        }
    },
}
</script>

<style scoped>
    li{
        color:deeppink;
    }
    .title{
        font-size: 50px;
        color: goldenrod;
    }

</style>