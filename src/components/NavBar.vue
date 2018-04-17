<template>
  <header class="navbar" role="banner">
    <router-link class="logo" to="/">
      <img :src="logoSrc" alt="Callisto Logo">
    </router-link>
    <nav role="navigation" aria-label="Main Menu">
      <ul class="nav-container">
        <li class="nav-item">
          <router-link class="nav-link" to="/get-involved">
            Get Involved
          </router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/who-we-are">
            Who We Are
          </router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/what-we-do">
            What We Do
          </router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/work-with-us">
            Work With Us
          </router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/donate">
            Donate
          </router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/contact">
            Contact
          </router-link>
        </li>
      </ul>
    </nav>
  </header>
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
  display: inline-block;
  margin: 0 -0.1rem 0 -0.1rem;
  padding: 0.5rem 1.5rem 1.5rem 1.5rem;
  color: $cl-white;
  border-bottom: 1px solid $cl-white;
  &:hover, &:focus {
    color: $cl-text-secondary;
    border-bottom: 1px solid $cl-text-secondary;
  }
  @include breakpoint(large) {
    width: 10rem;
  }
}
.nav-link {
  color: inherit;
  font-family: $monteserrat-stack;
  font-size: 0.8rem;
  font-weight: bold;
  text-transform: uppercase;
  text-decoration: none;
  text-align: center;
  letter-spacing: 1px;
  transition: color $time-fast;
}
</style>
