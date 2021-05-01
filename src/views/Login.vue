<template>
  <div class="login">
    <LoginComp />
    <RegisterComp />
  </div>
</template>

<script>
// @ is an alias to /src
import LoginComp from "@/components/LoginComp.vue";
import RegisterComp from "@/components/RegisterComp.vue";

export default {
  name: "Login",
  components: {
    LoginComp,
    RegisterComp,
  },
};
</script>

<style lang="scss" scoped>
.login {
  display: flex;
}
</style>
