<template>
  <div class="login">
    <NewPassword />
  </div>
</template>

<script>
// @ is an alias to /src
import NewPassword from "@/components/NewPasswordComp.vue";

export default {
  name: "NewCredentials",
  components: {
    NewPassword,
  },
};
</script>

<style lang="scss" scoped>
.login {
  display: flex;
  flex-direction: column;
}
</style>
