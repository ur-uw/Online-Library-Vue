<template>
  <header>
    <nav class="navbar">
      <ul class="navbar-menu">
        <li class="nav-item">
          <router-link class="nav-link" active-class="active" to="/"
            >Home
          </router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" active-class="active" to="/login"
            >Login
          </router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" active-class="active" to="/register"
            >Register
          </router-link>
        </li>
      </ul>
    </nav>
  </header>
  <!-- <router-link class="nav-link" active-class="active" to="/"
                >Home</router-link
              >
<router-link class="nav-link" active-class="active" to="/login"
                >Login</router-link
              >
<router-link class="nav-link" active-class="active" to="/register"
                >Register</router-link
              > -->
</template>



<script>
export default {
  name: "NavBar",
};
</script>

<style scoped lang="scss">
@import "../sass/app.scss";
.navbar {
  .navbar-menu {
    display: flex;
    list-style: none;
    .nav-item {
      .nav-link {
        color: $white;
        transition: 200ms;
        &:hover {
          color: $purple;
        }
      }
    }
  }
}
</style>

