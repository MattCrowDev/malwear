<template>
  <div class="login">
    <h1>Forgot Password?</h1>
    <p>
      Provide your account's email for which you want to reset your password.
    </p>
    <form action="/NewCredentials">
      <div class="formInput email">
        <i class="material-icons">person</i>
        <input placeholder="Email" type="email" name="" id="" />
      </div>
      <div class="formInput login">
        <button>Register</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "LoginComp",
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
  h1 {
    font-family: "Roboto", sans-serif;
    margin: 0.5rem;
  }
  .formInput {
    max-width: 100%;
    background: $inputColor;
    border-radius: 1rem;
    display: flex;
    align-items: center;

    box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.5);

    margin-block: 1rem;
    &:first-child {
      margin-top: 0;
    }

    i {
      margin: 0.5rem;
      margin-left: 0.75rem;
      user-select: none;
    }
    input {
      font-family: "Roboto", sans-serif;
      background: $inputBackgroundColor;
      font-size: 125%;
      width: 100%;
      height: auto;
      border: none;
      border-top-right-radius: 1rem;
      border-bottom-right-radius: 1rem;
      padding-block: 1rem;
      border-left: 0.1rem solid rgba(0, 0, 0, 0.5);
      &:focus {
        outline: none;
      }
      &::-webkit-outer-spin-button,
      &::-webkit-inner-spin-button {
        -webkit-appearance: none;
        margin: 0;
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
