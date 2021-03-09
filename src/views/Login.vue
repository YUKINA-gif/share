<template>
  <div id="login">
    <Header></Header>
    <div class="card">
      <h2>ログイン</h2>
      <form>
      <input type="email" name="email" placeholder="メールアドレス">
        <input type="password" name="password" placeholder="パスワード">
      <button @click="login">ログイン</button>
      </form>
    </div>
  </div>
</template>

<script>
import Header from '../components/Header';
export default {
  components:{
    Header
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