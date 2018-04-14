<template>
  <section class="navbar">
    <router-link class="logo" to="/">
      <img :src="logoSrc" alt="Callisto Logo">
    </router-link>
    <nav class="nav" aria-label="Main Menu">
      <ul>
        <li class="nav-item">
          <router-link class="nav-link" to="/get-involved">Get Involved</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/who-we-are">Who We Are</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/what-we-do">What We Do</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/work-with-us">Work With Us</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/donate">Donate</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/contact">Contact</router-link>
        </li>
      </ul>
    </nav>
  </section>
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
.navbar {
  position: absolute;
  width: 100vw;
  padding: 1rem;
  padding-left: 2rem;
  padding-right: 2rem;
  display: flex;
  flex-direction: row;
  flex-wrap: none;
  justify-content: center;
}
.logo {
  width: 100%;
  height: 100%;
  margin-left: 3rem;
  position: absolute;
}
.nav {
  border-bottom: 1px solid white;
  padding: 0.5rem;
}
.nav-item {
  display: inline-block;
  padding-left: 0.5rem;
  padding-right: 0.5rem;
}
.nav-link {
  color: white;
  font-weight: bold;
  text-transform: uppercase;
}
</style>
