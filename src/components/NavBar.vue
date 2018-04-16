<template>
  <nav class="navbar">
    <router-link class="logo" to="/">
      <img :src="logoSrc" alt="Callisto Logo">
    </router-link>
    <ul class="nav-container" aria-label="Main Menu">
      <li class="nav-item">
        <router-link class="nav-link" to="/get-involved">
          <h6 class="link-text"> Get Involved </h6>
        </router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/who-we-are">
          <h6 class="link-text"> Who We Are </h6>
        </router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/what-we-do">
          <h6 class="link-text"> What We Do </h6>
        </router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/work-with-us">
          <h6 class="link-text"> Work With Us </h6>
        </router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/donate">
          <h6 class="link-text"> Donate </h6>
        </router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/contact">
          <h6 class="link-text"> Contact </h6>
        </router-link>
      </li>
    </ul>
  </nav>
</template>

<script>
import logoSrc from '@/assets/callisto_logo.svg'

export default {
  name: 'NavBar',
  data () {
    return {
      logoSrc
    }
  }
}
</script>

<style scoped lang="scss">
@import '@/styles/_variables.scss';

.navbar {
  padding-top: 1rem;
}
.logo {
  position: absolute;
  top: 1.5rem;
  left: 3rem;
}
.nav-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  @include breakpoint(large) {
    flex-direction: column;
  }
}
.nav-item {
  margin: 0 -0.1rem 0 -0.1rem;
  padding: 0 1.5rem 1rem 1.5rem;
  display: inline-block;
  border-bottom: 1px solid $cl-white;
  text-align: center;
  @include breakpoint(large) {
    width: 10rem;
  }
}
.nav-link {
  color: $cl-white;
  font-weight: bold;
  text-transform: uppercase;
  text-decoration: none;
}
.link-text {
  font-size: 0.8rem;
  letter-spacing: 1px;
}
</style>
