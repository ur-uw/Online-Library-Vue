<template>
  <div class="row m-0 w-100 min-vh-100">
    <div class="col-md-6 col-sm-12">
      <NavBar />
      <div class="welcome-text text-center">WELCOME BACK</div>
      <div class="form-container">
        <form class="text-center" @submit.prevent="login">
          <div class="form-field">
            <span class="material-icons"> mail </span>
            <input
              type="email"
              id="email"
              class="form-input"
              name="email"
              autocomplete="off"
              placeholder="Email"
            />
          </div>
          <div class="form-field">
            <span class="material-icons"> lock </span>
            <input
              type="password"
              id="password"
              class="form-input"
              name="password"
              autocomplete="off"
              placeholder="Password"
            />
          </div>
          <button class="btn login-button">Login</button>
        </form>
        <div class="already-have-account-text">
          <h6 class="m-5">
            DON'T HAVE AN ACCOUNT?
            <router-link to="/register" class="text-purple"
              >REGISTER</router-link
            >
          </h6>
        </div>
      </div>
    </div>
    <div class="col-md-6 col-sm-12">
      <div class="img-container"></div>
    </div>
  </div>
</template>

<script>
import NavBar from "./NavBar.vue";
export default {
  name: "LoginForm",
  components: { NavBar },
  setup() {
    function login() {
      console.log("login");
    }

    return {
      login,
    };
  },
};
</script>

<style scoped lang="scss">
@import "../sass/app.scss";

.welcome-text {
  color: $white;
  font-size: 42px;
  font-weight: bold;
  position: relative;
  margin-top: 15%;
}
.form-container {
  position: relative;
  top: 10%;
  width: 100%;

  .form {
    width: 100%;
  }
  .form-field {
    background-color: $darkGrey;
    color: $white;
    margin: 1.5rem auto;
    padding: 0 1.5rem;
    border: none;
    border-radius: 10px;
    display: flex;
    height: 65px;
    width: 90%;
    align-items: center;
    .form-input {
      background-color: $darkGrey;
      color: $white;
      border: none;
      padding: 0.5rem 0.75rem;
      width: 100%;
      outline: none;
      &::placeholder {
        color: $white;
      }
    }
  }

  .login-button {
    background: $purple;
    color: $white;
    width: 90%;
    height: 65px;
    border-radius: 5px;
    margin: 0 auto;
    font-size: 34px;

    font-weight: 600;
    text-transform: uppercase;
    transition: 500ms;
    &:hover {
      background-color: darken($color: $purple, $amount: 2);
      transform: translateY(-2px);
    }
  }
}
.img-container {
  height: 100%;
  width: 100%;
  background: url("../assets/book-women.jpg");
  background-position: center;
  background-size: cover;
}
@media screen and (max-width: 500px) {
  .img-container {
    display: none;
  }
}
</style>