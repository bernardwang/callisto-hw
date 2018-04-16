<template>
  <section class="u-page splash typography">
    <NavBar />
    <div class="splash-text">
      <div class="title">
        <h1 class="title-display">
          Tech to Combat Sexual Assault
        </h1>
        <h3>
          We are stronger. Together.
        </h3>
        <button>
          Learn more
        </button>
      </div>
      <div class="quote">
        <p class="quote-text">
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
@import '@/styles/_color.scss';

.splash {
  min-height: 45rem;
  padding-bottom: 3rem;
  background-image: url('~@/assets/person_background.png'), url('~@/assets/faces_background.png');
  background-size: contain, cover;
  background-repeat: no-repeat;
  background-position: 25% 100%, center;
  color: $cl-white;
}
.splash-text {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
}
.quote {
  width: 35%;
  margin-top: 9rem;
  padding-right: 2rem;
}
.quote-text {
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
}
.title {
  width: 50%;
  margin-top: 18rem;
}
.title-display {
}
</style>
