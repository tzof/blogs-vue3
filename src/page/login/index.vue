<script setup lang="ts">
import { ref } from "vue";
const username = ref();
const password = ref();
const onClickLogin = () => {
  console.log(username.value, password.value);
};
const onClickRegister = () => {};
</script>
<template>
  <div class="login">
    <img src="@/assets/images/logo1.png" alt="" />
    <div class="login-box">
      <div class="username">
        <label>账号：</label>
        <el-input
          v-model="username"
          style="width: 240px"
          placeholder="请输入账号"
        />
      </div>
      <div class="passsword">
        <label>密码：</label>
        <el-input
          v-model="password"
          style="width: 240px"
          placeholder="请输入密码"
          show-password
        />
      </div>
      <div></div>
      <div class="submit">
        <el-button type="primary" round @click="onClickLogin">登录</el-button>
      </div>
      <div class="submit">
        <el-button round @click="onClickRegister">注册</el-button>
      </div>
    </div>
  </div>
</template>

<style scoped lang="less">
.login {
  width: 100%;
  height: 100%;
  background-image: url("@/assets/images/bj.png");
  background-size: 100% 100%;
  background-repeat: no-repeat;
  background-position: center center;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  img {
    height: 200px;
  }
  .login-box {
    width: 300px;
    padding: 40px;
    border: 1px solid black;
    border-radius: 20px;
    display: flex;
    flex-direction: column;
    div{
      margin-bottom: 10px;
      &:last-of-type{
        margin: 0;
      }
    }
    button{
      width: 100%;
    }
  }
}
</style>
