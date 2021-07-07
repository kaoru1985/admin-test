<template>
  <div class="header_wrapper">
    <a href="/">モルモット実験場</a>
    <button @click="logoutFunction()" class="button_normal">ログアウト</button>
  </div>
</template>
<script>
  export default {
    methods: {
      async logoutFunction () {
        await this.$auth.logout('laravelJWT');
        this.$router.push('/login')
      }
    }
  }
</script>
<style>
  .header_wrapper {
    height: 50px;
    background-color: #B1CCC2;
    line-height: 50px;
    padding: 0 20px;
  }
</style>
