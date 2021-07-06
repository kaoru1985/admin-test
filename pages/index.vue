<template>
  <div class="content-wrap">
    <p>君は会員だ！</p>
    <button @click="logoutFunction()" class="green">ログアウトする</button>
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
  .content-wrap {
    margin-top: 50px;
    display: flex;
    flex-flow: column;
    align-items: center;
  }
</style>
