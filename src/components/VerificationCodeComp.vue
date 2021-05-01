<template>
  <div class="login">
    <button class="closeButton"><i class="material-icons">close</i></button>
    <h1>Verification Code</h1>
    <p>Provide the 6 digit code that was sent to your email.</p>
    <form action="">
      <div class="formInput">
        <CodeInput :loading="false" class="input" />
      </div>
      <div class="formInput login">
        <button>Verify Code</button>
      </div>
    </form>
  </div>
</template>

<script>
import CodeInput from "vue-verification-code-input";

export default {
  name: "LoginComp",
  components: {
    CodeInput,
  },
};
</script>

<style scoped lang="scss">
@import "@/assets/styles/_variables.scss";

.login {
  background: $backgroundColor;
  color: $textColor;
  display: flex;
  justify-content: center;
  flex-direction: column;
  margin-inline: auto;
  width: 70vw;
  max-width: $maxWidth;
  .closeButton {
    width: 4.5rem;
    height: 4.5rem;
    border-radius: 50%;
    margin-left: auto;
    background: $inputColor;
    border: 0.1rem solid rgba(0, 0, 0, 0.2);
    box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.5);
    cursor: pointer;
    &:hover {
      background: rgba(0, 0, 0, 0.1);
    }
    &:focus {
      outline: none;
    }
  }
  h1 {
    font-family: "Roboto", sans-serif;
    margin: 0.5rem;
  }
  .formInput {
    max-width: 100%;
    border-radius: 1rem;
    display: flex;
    justify-content: center;

    margin-bottom: 1rem;
    .input {
      margin-top: 0;
      box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.5);
      border-radius: 10px;
      input {
        background: $inputBackgroundColor;
      }
    }
    button {
      font-family: "Roboto", sans-serif;
      width: 100%;
      padding: 1rem;
      font-size: 125%;
      border-radius: 1rem;
      border: none;
      cursor: pointer;
      box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.5);

      background: $textColor;
      color: $inputBackgroundColor;
      &:hover {
        background: rgba(0, 0, 0, 0.8);
      }
      &:focus {
        outline: none;
      }
    }
  }
}
@media screen and (max-width: 768px) {
  .login {
    width: 90vw;
  }
}
</style>
