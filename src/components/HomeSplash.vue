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
        <Button variant="primary">
          Learn more
        </Button>
      </div>
      <div class="text right">
        <p class="right-quote">
          'why are you questioning the victim here? let's flip it. let's talk about what the predator is doing.'
        </p>
      </div>
    </div>
    <div class="scroll">
      <p class="scroll-text">
        Scroll down
      </p>
    </div>
  </section>
</template>

<script>
import Button from '@/components/core/Button'
import NavBar from '@/components/NavBar'

export default {
  name: 'HomeSplash',
  components: {
    Button,
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
  margin-top: 16rem;
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
.scroll {
  position: absolute;
  width: 3rem;
  left: 41%;
  bottom: 0rem;
  transition: transform $time-normal;
  &:hover {
    transform: translateY(4px)
  }
}
.scroll-text {
  transform: rotate(-90deg);
  text-transform: uppercase;
  font-weight: 500;
  font-size: 0.7rem;
  text-align: center;
  cursor: pointer;
}
</style>
