<template>
  <section class="navbar">
    <router-link class="logo" to="/">
      <img :src="logoSrc" alt="Callisto Logo">
    </router-link>
    <nav class="nav" aria-label="Main Menu">
      <ul>
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
  padding-top: 1rem;
  display: flex;
  flex-direction: row;
  flex-wrap: none;
  justify-content: center;
}
.logo {
  position: absolute;
  left: 3rem;
}
.nav {
  border-bottom: 1px solid white;
}
.nav-item {
  display: inline-block;
  padding-left: 1.5rem;
  padding-right: 1.5rem;
}
.nav-link {
  color: white;
  font-weight: bold;
  text-transform: uppercase;
  text-decoration: none;
}
.link-text {
  font-size: 0.8rem;
  letter-spacing: 1px;
}
</style>
