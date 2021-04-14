<template>
  <div class="login">
    <ForgotPassword />
  </div>
</template>

<script>
// @ is an alias to /src
import ForgotPassword from "@/components/ForgotPasswordComp.vue";

export default {
  name: "ForgotPass",
  components: {
    ForgotPassword,
  },
};
</script>

<style lang="scss" scoped>
.login {
  display: flex;
  flex-direction: column;
}
</style>
