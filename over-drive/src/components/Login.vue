<template>
  <div>
    <div class="bg-login"></div>
    <div class="login-form">
      <header class="center">
        <div class="logo"></div>
        <h2>over drive</h2>
      </header>
      <el-form>
        <el-form-item>
          <el-input :placeholder="$t('username')" v-model="loginInfo.username"></el-input>
        </el-form-item>
        <el-form-item>
          <el-input :placeholder="$t('password')" v-model="loginInfo.password" type="password"></el-input>
        </el-form-item>
        <el-form-item>
          <el-button class="btn-login" type="primary" nativeType="submit" @click.prevent="login" v-text="$t('login')"></el-button>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      loginInfo: {
        username: '',
        password: ''
      }
    }
  },
  methods: {
    login() {
      console.info(`login username: ${this.loginInfo.username} password: ${this.loginInfo.password}`)
    }
  }
}
</script>

<style>
  .login-form {
    text-align: center;
    border-radius: 5px;
    padding: 50px 50px 20px;
    background-color: rgba(255, 255, 255, 0.85);
    width: 400px;
    margin: 20vh auto 0;
    position: relative;
  }
  .login-form {
    width: 300px;
  }
  .bg-login {
    background: url('../assets/login.jpg');
    background-size: cover;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
  .btn-login {
    width: 100%;
  }
  .logo {
    display: inline-block;
    background: url('../assets/logo.jpg');
    height: 100px;
    width: 100px;
  }
</style>

<i18n>
  {
    "zh": {
      "username": "用户名",
      "password": "密码",
      "login": "登陆"
    }
  }
</i18n>
