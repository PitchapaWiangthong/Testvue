<template>
  <div id = "demo4">
      <h2>{{firstname}}</h2>
      <h2>{{lastname}}</h2>
      <h2>{{fullname}}</h2>

      <h1 style="background-color:gray;">
          Random Num from computed property: {{getrandomno}}
      </h1>
      <h1 style="background-color:gray;">
          Random Num from computed property: {{getrandomno}}
      </h1>
      <h1 style="background-color:gray;">
          Random Num from computed property: {{getrandomno}}
      </h1>
        <!-- สำหรับ method ต้องมี () ข้างหลัง -->
      <h1>Random Num from method:{{getrandomno1()}}</h1>
      <h1>Random Num from method:{{getrandomno1()}}</h1>

  </div>
</template>

<script>
export default {
name:"Demo4",
methods: {
     //ค่าที่แรนดอมออกมาจะแรนดอมใหม่เสมอ
    getrandomno1: function(){
        return Math.random();
    }
},
   

data() {
    return {
        firstname:"Pitchapa",
        lastname:"Wiangthong"
    }
},
computed:{ 
    //ไม่ต้องใส่วงเล็บเปิดปิด,ค่าที่ได้จะอัปเดตตามค่าล่าสุด
    fullname(){
        //สามารถเรียกในลักษณะของตัวแปร เรียกโดยไม่ใส่วงเล็บ
        return this.firstname + " " + this.lastname
    },
    getrandomno(){
        return Math.random();
    }
}
}
</script>

<style>

</style>