<template>
  <div class="login">
    <h1>New Credentials</h1>
    <p>Set your new password.</p>
    <form action="/login">
      <div class="formInput password">
        <i class="material-icons">lock</i>
        <input
          placeholder="New Password"
          :type="[showPassword ? 'text' : 'password']"
          name=""
          id="password"
        />
        <i
          class="material-icons eye"
          :class="[showPassword ? '' : 'hidden']"
          @click="showPassword = !showPassword"
          >remove_red_eye</i
        >
      </div>
      <div class="formInput password">
        <i class="material-icons">lock</i>
        <input
          placeholder="Confirm Password"
          :type="[showPassword ? 'text' : 'password']"
          name=""
          id="password"
        />
        <i
          class="material-icons eye"
          :class="[showPassword ? '' : 'hidden']"
          @click="showPassword = !showPassword"
          >remove_red_eye</i
        >
      </div>
      <div class="formInput login">
        <button>Confirm</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "LoginComp",
  props: {},
  data() {
    return {
      showPassword: false,
    };
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
    .blank {
      margin-left: 0.5rem;
    }
    .eye {
      margin-left: 0.5rem;
      cursor: pointer;
      position: relative;
      &.hidden::after {
        content: "";
        position: absolute;
        width: 5px;
        height: 100%;
        left: 40%;
        transform: rotate(45deg);
        background: $textColor;
        border-radius: 2.5px;
      }
    }
    input {
      font-family: "Roboto", sans-serif;
      background: $inputBackgroundColor;
      font-size: 125%;
      width: 100%;
      height: auto;
      border: none;
      border-radius: 0;
      padding-block: 1rem;
      border-inline: 0.1rem solid rgba(0, 0, 0, 0.5);

      &:focus {
        outline: none;
      }
    }
    button {
      font-family: "Roboto", sans-serif;
      padding: 1rem;
      width: 100%;
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
  .postFormItems {
    font-family: "Roboto", sans-serif;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-inline: 0.5rem;
    a {
      color: black;
      text-decoration: none;
      &:hover {
        text-decoration: underline;
        color: black;
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
