<template>
  <div class="flex">
  <div class="home left">
    <SideNavi />
    <ShareMessage />
  </div>
  <div class="right">
    <div class="title">
      <p>プロフィール</p>
    </div>
    <div>
      <div class="profile">
        <div class="flex-profile">
          <p class="profile-name">{{name}}</p>
          <div @click="edit">
            <button>変更する</button>
          </div>
        </div>
        <p class="text" v-if="active">{{profile}}</p>
        <input type="text" v-model="profile" v-else />
    </div>
    <Message />
    </div>
  </div>
  </div>
</template>

<script>
import SideNavi from '../components/SideNavi';
import Message from "../components/Message";
import ShareMessage from "../components/ShareMessage";

export default {
  components:{
    SideNavi,Message,ShareMessage
  },
  data() {
    return {
      active:true,
      name:"太郎",
      profile:"太郎です",
    };
  },
};
</script>


<style scoped>
.left {
  width: 22%;
  height: 100vh;
}
.right {
  width: 78%;
  height: 100vh;
}
.flex {
  display: flex;
}
.profile {
  padding: 20px;
  border-bottom: solid 1px white;
  border-left: 1px solid white;
}
.profile-name {
  font-size: 24px;
}
.title {
  border-bottom: 1px solid white;
  border-left: 1px solid white;
  padding: 15px;
}
.title p {
  font-size: 20px;
  font-weight: bold;
}
.flex-profile {
  display: flex;
  justify-content: space-between;
}
button {
  width: 100px;
  text-align: center;
  padding: 8px 0 10px;
  color: #fff;
  background-color: #5419da;
  border-radius: 25px;
  display: block;
  margin: 0 0 0 auto;
}
</style>