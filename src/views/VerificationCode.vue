<template>
  <div class="login">
    <VerificationCode />
  </div>
</template>

<script>
// @ is an alias to /src
import VerificationCode from "@/components/VerificationCodeComp.vue";

export default {
  name: "VerificationCode",
  components: {
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
