<template>
  <div id="demo6">
      <form v-on:submit.prevent="submit">

            <!-- Firstname -->
          <div style="margin-top: 16px;">
              <label for="first_name">Firstname</label>
              <input style="margin-left: 10px;" type="text" name="first_name" v-model="applicant.first_name">
          </div>
            <!-- Lastname -->
          <div style="margin-top: 16px;">
              <label for="last_name">Lastname</label>
              <input style="margin-left: 10px;" type="text" name="last_name" v-model="applicant.last_name">
          </div>
            <!-- Sex -->
          <div style="margin-top: 20px;">
              <label for="sex">Female</label>
              <input style="margin-left: 10px;" type="radio" name="sex" value="female" v-model="applicant.sex">
          </div>

          <div style="margin-top: 20px;">
              <label for="sex">Male</label>
              <input style="margin-left: 23px;" type="radio" name="sex" value="male" v-model="applicant.sex">
          </div>
            <!-- Course -->
            <div style="margin-top: 20px;">
                <select name="courses" v-model="applicant.course">
                    <option value="react">React</option>
                    <option value="angular">Angular</option>
                    <option value="vuejs">Vue</option>
                </select>
            </div>

            <button type="submit" >Submit</button>
            <button type="button" @click="clear">Reset</button>

      </form>
      <div style="margin-top: 16px; color: red;">#Spy {{JSON.stringify(applicant)}}</div>

  </div>
</template>

<script>
export default {
name:"Demo6",
data() {
    return {
        applicant: {
            first_name: "",
            last_name: "",
            sex: "female",
            course: "react"
        }
    }
},
methods: {
    submit(){
        alert(JSON.stringify(this.applicant))
    },
    clear(){
        this.applicant = {
            first_name: "",
            last_name: "",
            sex: "female",
            course: "react",
        }
    }
},

}
</script>

<style>

</style>