<template>
  <div class="header_wrapper">
    <NuxtLink to='/' class="header_title"><font-awesome-icon icon="poo" style="font-size: 18px" /> モルモット実験場</NuxtLink>
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
    display: flex;
    justify-content: space-between;
    height: 50px;
    background-color: #B1CCC2;
    line-height: 50px;
    padding: 0 20px;
  }
  .header_title {
    color: #134633;
  }
</style>
