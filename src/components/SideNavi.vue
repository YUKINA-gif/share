<template>
  <div id="sideMenu">
    <h1><img class="logo" src="../assets/logo.png" alt="logo"></h1>
    <div class="flex icon-field" @click="$router.push('/home')">
      <img class="icon" src="../assets/home.png" alt="home">
      <p>ホーム</p>
    </div>

    <div class="flex icon-field" @click="$router.push('/profile')">
      <img class="icon" src="../assets/profile.png" alt="profile">
      <p>プロフィール</p>
    </div>

    <div class="flex icon-field" @click="$store.dispatch('logout')">
      <img class="icon" src="../assets/logout.png" alt="logout">
      <p>ログアウト</p>
    </div>

  </div>
</template>

<style scoped>
a{
  display: block;
  display: flex;
}

.sideMenu {
  margin: 20px;
}
.flex {
  display: flex;
}
.logo {
  width: 100px;
}
.icon-field {
  margin-top: 15px;
  cursor: pointer;
}
.icon {
  width: 25px;
}
.icon-field p {
  font-size: 16px;
  padding-left: 15px;
}
</style>