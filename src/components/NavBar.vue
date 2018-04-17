<template>
  <header class="navbar" role="banner">
    <router-link class="logo" to="/">
      <img class="logo-img" :src="logoSrc" alt="Callisto Logo">
    </router-link>
      <NavBarIcon class="menu-icon" :open="menuOpen" :onClick="toggleMenu"/>
    <nav role="navigation" aria-label="Main Menu">
      <ul :class="navMenuClass">
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
import NavBarIcon from '@/components/NavBarIcon'

export default {
  name: 'NavBar',
  components: { NavBarIcon },
  data () {
    return {
      logoSrc,
      menuOpen: false,
    }
  },
  computed: {
    navMenuClass: function () {
      return {
        'nav-menu': true,
        'nav-menu-open': this.open
      }
    }
  },
  methods: {
    toggleMenu: function () {
      this.menuOpen = !this.menuOpen
      this.navMenuClass['nav-menu-open'] = this.menuOpen
      console.log(this.menuOpen)
    }
  }
}
</script>

<style scoped lang="scss">
@import '@/styles/_variables.scss';

.navbar {
  padding-top: 1rem;

  // Breakpoint for menu transition
  @include breakpoint(large) {
    .menu-icon {
      display: block;
    }
    .nav-menu {
      flex-direction: column;
      display: none;
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
    }
    .nav-menu-open {
      display: flex;
      background-color: rgba($cl-text-primary, 0.5);
      padding: 1rem 0 2rem 0;
    }
    .nav-item {
      width: 10rem;
    }
  }
}
.logo {
  position: absolute;
  top: 1.5rem;
  left: 3rem;
}
.nav-menu {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  margin: 0;
  z-index: 2;
}
.nav-item {
  display: inline-block;
  margin: 0 -0.1rem 0 -0.1rem;
  padding: 1.5rem;
  color: $cl-white;
  border-bottom: 1px solid $cl-white;
  text-align: center;
  &:hover, &:focus {
    color: $cl-text-secondary;
    border-bottom: 1px solid $cl-text-secondary;
  }
}
.nav-link {
  color: inherit;
  font-family: $monteserrat-stack;
  font-size: 0.8rem;
  font-weight: bold;
  text-transform: uppercase;
  text-decoration: none;
  letter-spacing: 1px;
  transition: color $time-fast;
}
</style>
