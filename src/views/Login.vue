<template>
  <div class="login-container">
    <div class="login-wrap">
      <div class="login-title">系统登录</div>
      <el-form :model="ruleForm" class="login-form">
        <el-form-item prop="user">
          <el-input
            v-model="ruleForm.user"
            type="text"
            placeholder="用户名"
            autocomplete="off"
          />
        </el-form-item>
        <el-form-item prop="pass">
          <el-input
            placeholder="密码"
            v-model="ruleForm.pass"
            type="password"
            autocomplete="off"
          />
        </el-form-item>
        <el-form-item>
          <el-button type="primary" @click="submitForm()" class="submit-btn">登录</el-button>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>

<script>
import { reactive, ref } from "vue";
export default {
  name: "Login",
  setup() {
    let ruleForm = reactive({
      user: "",
      pass: "",
    });
    function submitForm() {}
    return {
      ruleForm,
      submitForm,
    };
  },
};
</script>

<style lang="scss" scoped>
.login-container {
  position: relative;
  width: 100%;
  height: 100vh;
  background-color: #235bae;
  background-image: url(../assets/login_bg.a62d8a.jpg);
  background-size: cover;
  .login-wrap {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 1;
    width: 350px;
    overflow: hidden;
    background: hsla(0, 0%, 100%, 0.4);
    border-radius: 5px;
    .login-title {
      width: 100%;
      font-size: 20px;
      line-height: 50px;
      color: #fff;
      text-align: center;
      border-bottom: 1px solid #ddd;
    }
    .login-form {
      padding: 30px;
      .submit-btn{
        width: 100vh;
      }
    }
  }
}
</style>