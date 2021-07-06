<template>
  <div class="login-wrap">
    <p>{{ result }}</p>
    <input v-model="uuid" type="text" placeholder="秘密のかぎ">
    <button @click="loginFunction()" type="submit" class="green">ログイン</button>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        result: '',
        uuid: '',
      }
    },
    
    methods: {
      async loginFunction () {
        try {
          const response = await this.$auth.loginWith('laravelJWT', { data: { local_uuid: this.uuid } });
          console.log('ログインできた〜！');
          console.log(response);
          this.$router.push('/')
        }catch (error) {
          console.log(error);
          this.result = 'ログインに失敗しました'
        }
      },
      
      // ↑のように.thenで書かれていた処理をasyncとawaitで書き直すのに慣れるとよい(順番に処理してくれる＆ぱっと見わかりやすい)
    // tryは字のとおり順番に試してみてくれる、だめだったら「だめです！」をcatchしてくれる
    
    // uuidのメモ：SHJJRfOmS1oFPEk00JJKqvXEKCmF50UFrZMYWglbftQqHNFd9vrEK13PEklMQuIG
  
    // async formLogin () {
    //   axios.post()
    //           .then((res) => {
    //             console.log(res);
    //             this.result = 'ログインできました！';
    //           })
    //
    //   // 上記と同じ処理
    //   // const res = await axios.post(url, this.posts)
    //   // console.log(res);
    //   // this.result = '成功しました'
    //
    // }
  }
}
</script>
<style>
  .login-wrap {
    width: 300px;
    display: flex;
    flex-flow: column;
    align-items: center;
    margin: 20px auto 0;
  }
  input {
    width: 80%;
    height: 2rem;
    padding: 0 10px;
    margin-bottom: 10px;
  }
</style>
