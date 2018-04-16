<template>
  <section class="u-page splash typography">
    <NavBar />
    <div class="text-container">
      <div class="text left">
        <h1 class="left-display">
          Tech to Combat Sexual Assault
        </h1>
        <h3>
          We are stronger. Together.
        </h3>
        <button>
          Learn more
        </button>
      </div>
      <div class="text right">
        <p class="right-quote">
          'why are you questioning the victim here? let's flip it. let's talk about what the predator is doing.'
        </p>
      </div>
    </div>
  </section>
</template>

<script>
import NavBar from '@/components/NavBar'

export default {
  name: 'HomeSplash',
  components: {
    NavBar
  }
}
</script>

<style scoped lang="scss">
@import '@/styles/_variables.scss';

.splash {
  min-height: 45rem;
  padding-bottom: 3rem;
  background-image: url('~@/assets/person_background.png'), url('~@/assets/faces_background.png');
  background-size: contain, cover;
  background-repeat: no-repeat;
  background-position: 25% 100%, center;
  color: $cl-white;
}
.text-container {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  @include breakpoint(medium) {
    flex-direction: column;
  }
}
.right {
  width: 35%;
  margin-top: 9rem;
  padding-right: 2rem;
}
.left {
  width: 50%;
  margin-top: 18rem;
}
.text {
  @include breakpoint(medium) {
    width: 100%;
    padding: 0;
    margin-top: 3rem;
  }
}
.left-display {
}
.right-quote {
  position: relative;
  font-size: 1.414rem;
  &:before {
    content: "";
    position: absolute;
    border-top: 1px solid $cl-text-secondary;
    top: 50%;
    right: -12rem;
    width: 12rem;
  }
  @include breakpoint(medium) {
    &:before {
      border: none;
    }
  }
}
</style>
