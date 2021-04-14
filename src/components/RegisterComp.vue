<template>
  <div class="login">
    <h1>Hello!</h1>
    <h1>Register To Get Started</h1>
    <form action="/">
      <div class="formInput">
        <i class="material-icons">person_add</i>
        <input placeholder="Name" required type="text" name="" id="name" />
      </div>
      <div class="formInput email">
        <i class="material-icons">person</i>
        <input
          placeholder="Email"
          required
          type="email"
          name=""
          id="newEmail"
        />
      </div>
      <div class="formInput password">
        <i class="material-icons">lock</i>
        <input
          placeholder="Password"
          required
          v-bind:value="password"
          v-on:input="password = $event.target.value"
          type="password"
          name=""
          id="newPassword"
        />
      </div>
      <div class="formInput password">
        <i class="material-icons">lock</i>
        <input
          placeholder="Confirm Password"
          required
          v-bind:value="confPassword"
          v-on:input="confPassword = $event.target.value"
          type="password"
          name=""
          id="confPassword"
        />
      </div>
      <p class="passMatchErr" v-if="password != confPassword">
        Passwords must match.
      </p>
      <div class="formInput">
        <i class="material-icons">local_phone</i>
        <input placeholder="Phone Number" type="number" name="" id="phone" />
      </div>
      <div class="formInput">
        <i class="material-icons">pin_drop</i>
        <input placeholder="Address" type="address" name="" id="address" />
      </div>
      <div class="formInput login">
        <button :class="[password == confPassword ? enabled : 'disabled']">
          Register
        </button>
      </div>
    </form>
    <div class="postFormItems">
      <div>
        <p>Already have an account? <a href="">Login</a></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LoginComp",
  data() {
    return {
      password: "",
      confPassword: "",
    };
  },
};
</script>

<style scoped lang="scss">
@import "@/assets/styles/_variables.scss";
.passMatchErr {
  color: red;
  text-align: left;
}
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
    text-align: left;
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
    &:last-child {
      background: none;
      color: $inputBackgroundColor;
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

      &.disabled {
        z-index: -1;
        cursor: unset;
        background: rgba(25, 25, 25, 0.9);
        &:hover {
          background: rgba(25, 25, 25, 0.9);
        }
        p {
          margin: 0;
          z-index: 1000;
        }
      }
      &:hover {
        background: rgba(0, 0, 0, 0.8);
      }
      background: $textColor;
      color: $inputBackgroundColor;
      &:focus {
        outline: none;
      }
      p {
        margin: 0;
        z-index: 1;
      }
    }
  }
  .postFormItems {
    font-family: "Roboto", sans-serif;
    display: flex;
    flex-direction: row;
    justify-content: center;
    margin-inline: 0.5rem;
    color: rgba(0, 0, 0, 0.7);
    a {
      color: black;
      text-decoration: none;
      font-weight: bold;
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
