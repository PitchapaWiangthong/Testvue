<template>
  <div>
      <h1>{{Header}}</h1>
      <!-- สร้างช่องสำหรับใส่ข้อมูล -->
      <input v-model="message" type="text" placeholder="Enter your name">
      <!-- สร้างปุ่มสำหรับคลิ้ก -->
    <button @click="message='' ">Reset</button>
  </div>
</template>

<script>
export default {
name : "demo1",
data() {
    return {
        Header : "Demo1",
        message: ""
    }
},
}
</script>
<style>

</style>