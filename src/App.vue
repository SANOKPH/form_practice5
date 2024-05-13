<template>
  <RegisterForm />
  
</template>

<script>
import RegisterForm from './components/RegisterForm.vue';

export default {
  name: 'App', 
  components: {
    RegisterForm
  }
}
</script>

<style>

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
