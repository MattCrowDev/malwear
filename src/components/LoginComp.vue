<template>
  <div class="login">
    <h1>Hello Again!</h1>
    <h1>Welcome Back</h1>
    <form action="">
      <div class="formInput email">
        <i class="material-icons">person</i>
        <input type="email" name="" id="" />
      </div>
      <div class="formInput password">
        <i class="material-icons">lock</i>
        <input type="password" name="" id="" />
      </div>
      <div class="formInput login">
        <button>Login</button>
      </div>
    </form>
    <div class="postFormItems">
      <div class="item1">
        <input type="checkbox" name="" id="rememberMe" />
        <label for="rememberMe">Remeber me</label>
      </div>
      <div class="item2">
        <a href="#">Forgot Password</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LoginComp",
  props: {},
  data() {
    return {};
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
$inputColor: #ddd;
$inputBackgroundColor: #eee;
$textColor: #000;
$backgroundColor: rgba(0, 0, 0, 0);
.login {
  background: $backgroundColor;
  color: $textColor;
  display: flex;
  justify-content: center;
  flex-direction: column;
  margin-inline: auto;
  width: 70vw;
  max-width: 2048px;
  h1 {
    margin: 0.5rem;
    text-align: left;
  }
  .formInput {
    max-width: 100%;
    background: $inputColor;
    border-radius: 1rem;
    display: flex;

    margin-block: 0.5rem;
    &:first-child {
      margin-top: 0;
    }

    i {
      margin: 0.5rem;
      margin-left: 0.75rem;
    }
    input {
      background: $inputBackgroundColor;
      font-size: 125%;
      width: calc(100% - 4.25rem);
      border: none;
      border-inline: 0.1rem solid rgba(0, 0, 0, 0.5);
      &:focus {
        outline: none;
      }
    }
    button {
      padding: 0.75rem;
      border-radius: 1rem;
      border: none;
      cursor: pointer;
      &:hover {
        background: rgba(0, 0, 0, 0.1);
      }
      &:focus {
        outline: none;
      }
    }
  }
  .postFormItems {
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
</style>
