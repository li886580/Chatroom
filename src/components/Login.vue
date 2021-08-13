<template>
  <div class="loginPage">
    <div class="account">
      <p class="loginPage__p">帳號</p>
      <input class="account__input" type="text">
    </div>
    <div class="pwd">
      <p class="loginPage__p">密碼</p>
      <input class="pwd__input" type="text">
    </div>
    <a class="login">登入</a>
  </div>
</template>

<script>
export default {
  name: 'Login',

}
</script>

<style scoped src="../assets/css/Login.css">
</style>