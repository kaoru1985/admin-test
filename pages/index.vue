<template>
  <div class="content-wrap">
    <p>君は会員だ！</p>
    <button @click="logoutFunction()">ログアウトする</button>
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
  button {
    color: #fff;
    background-color: #00cd81;
    border: none;
    border-radius: 20px;
    padding: .5rem 2rem;
  }
  button:hover {
    opacity: .8;
  }
</style>
