<template>
  <div class="header flex">
    <img src="../assets/logo.png" alt="logo">
    <nav>
      <ul class="flex">
        <li @click="$router.push('/signup')">新規登録</li>
        <li @click="$router.push('/')">ログイン</li>
      </ul>
    </nav>
  </div>
</template>

<style scoped>
li{
  margin-right: 20px;
  cursor: pointer;
}
.flex{
  display: flex;
  justify-content: space-between;
}
img{
  cursor: pointer;
  width: 150px;
}
.header{
  margin:20px;
}

</style>