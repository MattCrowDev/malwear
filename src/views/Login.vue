<template>
  <div class="login">
    <LoginComp />
    <RegisterComp />
    <ForgotPassword />
    <VerificationCode />
  </div>
</template>

<script>
// @ is an alias to /src
import LoginComp from "@/components/LoginComp.vue";
import RegisterComp from "@/components/RegisterComp.vue";
import ForgotPassword from "@/components/ForgotPassword.vue";
import VerificationCode from "@/components/VerificationCode.vue";

export default {
  name: "Login",
  components: {
    LoginComp,
    RegisterComp,
    ForgotPassword,
    VerificationCode,
  },
};
</script>

<style lang="scss" scoped>
.login {
  display: flex;
  flex-direction: column;
}
</style>
