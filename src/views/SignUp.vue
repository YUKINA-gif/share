<template>
  <div id="signup">
    <Header></Header>
    
    <form class="card">
      <h2>新規登録</h2>
      <input type="text" name="username" id="username" placeholder="ユーザーネーム" v-model="username">
      <input type="text" name="profile" id="profile" placeholder="プロフィール" v-model="profile">
      <input type="email" name="email" id="email" placeholder="メールアドレス" v-model="email">
      <input type="password" name="password" id="password" placeholder="パスワード" v-model="password">
      <button @click="signUp">新規登録</button>
    </form>
    
  </div>
</template>

<script>
import axios from 'axios';
import Header from '../components/Header';
export default {
  components:{
    Header
  },
  data() {
    return {
      username : "",
      profile : "",
      email : "",
      password : "",
    }
  },
  methods: {
    async signUp(){
      const sendData = {
        username:this.username,
        profile:this.profile,
        email:this.email,
        password:this.password,
      };
      await axios.post("http://",sendData);
      await this.getData;
    }
  },
}
</script>

<style scoped>
button {
 width: 100px;
 text-align: center;
 padding: 8px 0 10px;
 color: #fff;
 background-color: #5419da;
 border-radius: 25px;
 cursor: pointer;
}
.card {
 margin: 100px auto;
 width: 350px;
 background: #fff;
 border-radius: 5px;
 padding: 20px;
}
.card h2 {
 color: black;
 font-weight: bold;
 text-align: center;
}
input {
 margin-top: 15px;
 width: 80%;
 border-radius: 10px;
 padding: 10px;
 border: 1px solid black;
 color: black;
}
form {
 text-align: center;
}
form button {
 margin-top: 15px;
}
</style>