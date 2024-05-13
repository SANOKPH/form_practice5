<template>
  <div class="container">
    <div class="left-box">
      <div class="header">
        <h1>Register</h1>
      </div>
      <div class="form-group">
        <label>First Name:</label>
        <input type="text" class="controls" placeholder="Enter First Name" v-model="FirstName" >
      </div>
      <div class="form-group">
        <label>Last Name:</label>
        <input type="text" class="controls" placeholder="Enter Last Name" v-model="LastName" >
      </div>
      <div class="form-group">
        <label>Gender:</label>
        <select class="controls" v-model="Gender" >
          <option value="Female">Female</option>
          <option value="Male">Male</option>
          <option value="Other">Other</option>
        </select>
      </div>
      <div class="form-group">
        <label>Age:</label>
        <input type="number" class="controls" placeholder="Enter Age" v-model="Age" >
      </div>
      <div class="form-group">
        <label>Score:</label>
        <input type="number" class="controls" placeholder="Enter Score" v-model="Score">
      </div>
    </div>
    <div class="right-box">
        <ul>
          <li class="info">First name:{{FirstName}} </li>
          <li class="info">Last name: {{LastName}}</li>
          <li class="info" >Full name:{{FullName}} </li>
          <li class="info">Gender: {{Gender}} </li>
          <li class="info">Age:{{Age}}</li>
          <li>{{CheckAge}} </li>
          <li class="info">Score:{{Score}} </li>
          <li>{{CheckScore}} </li>
        </ul>
    </div>
 </div>
</template>

<script>
export default {
  name:"RegisterForm",
  data() {
    return {
      FirstName:"",
      LastName:"",
      Gender:null,
      Age:null,
      Score:null

    }
  },
  computed:{
    FullName(){
      return this.FirstName + " - " + this.LastName;

    },
    CheckAge(){
      const age = this.Age
      if(age > 0 && age < 15){
        return "You are child";

      }else if(age >=15 && age<18 ){
        return "You are young";

      }else if(age >=18 && age <30 ){
        return "You are adualt";

      }else if(age >30){
        return "You are old";

      }else{
        return null;

      }
    },

    CheckScore(){
      const score = this.Score;
      if(score >= 0 && score <= 49){
        return "F"
      }else if(score >= 50 && score <60){
        return "E"

    }else if(score >=60 && score<70){
      return "D"
    }else if(score >=80 && score <90){
      return "C"
    }else if (score >= 90 && score < 100 ){
      return "B"
    }else{
      return "A"
    }
  }
}
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  display: flex;
  justify-content: center;
}
.left-box {
  border: 2px solid orange;
  padding: 10px;
}
.right-box {
  border: 2px solid teal;
  padding: 10px;
  width: 30%;
}
.form-group {
  margin-bottom: 10px;
  display: flex;
  flex-direction: column;
  text-align: left;
}
label {
  padding-bottom: 10px;
}
.controls {
  padding: 10px;
  width: 500px;
  box-sizing: border-box;

}
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  text-align: left;
}
ul .info {
  padding: 10px;
  margin-bottom: 10px;
  border-bottom: 1px solid #ccc;
}
</style>
