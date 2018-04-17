<template>
  <section class="u-page splash">
    <NavBar />
    <div class="article-container">
      <article class="article left">
        <h1 class="left-display">
          Tech to Combat Sexual Assault
        </h1>
        <p class="left-headline">
          We are stronger. Together.
        </p>
        <Button variant="primary">
          Learn more
        </Button>
      </article>
      <aside class="article right" role="complementary">
        <p class="right-quote headline">
          'why are you questioning the victim here? let's flip it. let's talk about what the predator is doing.'
        </p>
      </aside>
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
  position: relative;
  min-height: 100vh;
  padding-bottom: 3rem;
  background-image: url('~@/assets/person_background.png'), url('~@/assets/faces_background.png');
  background-size: contain, cover;
  background-repeat: no-repeat;
  background-position: 25% 100%, center;
  color: $cl-white;
  @include breakpoint(medium) {
    flex-direction: column;

    // Remove lines and scroll
    // TODO: find better way to handle responsiveness for visual elements
    .right-quote:before {
      border: none;
    }
    .scroll {
      display: none;
    }
  }
}
.article-container {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
}
.article {
  @include breakpoint(medium) {
    width: 100%;
    padding: 0;
    margin-top: 3rem;
  }
}
.right {
  width: 35%;
  margin-top: 9rem;
  padding-right: 2rem;
}
.left {
  width: 50%;
  margin-top: 14rem;
}
.left-display {
  font-family: $playfair-stack;
  font-weight: 900;
  margin-bottom: 1.5rem;
}
.left-headline {
  font-family: $oswald-stack;
  font-weight: 500;
  font-size: 2rem;
  margin-top: 1.5rem;
}
.right-quote {
  position: relative;
  padding-right: 3rem;
  font-family: $oswald-stack;
  font-size: 1.414rem;
  font-style: italic;
  &:before {
    content: "";
    position: absolute;
    border-top: 1px solid $cl-text-secondary;
    top: 50%;
    right: -11rem;
    width: 13rem;
  }
}
.scroll {
  position: absolute;
  width: 3rem;
  left: 42%;
  bottom: 1rem;
  transition: transform $time-normal;
  &:hover {
    transform: translateY(4px)
  }
}
.scroll-text {
  transform: rotate(-90deg);
  text-transform: uppercase;
  font-family: $monteserrat-stack;
  font-weight: 500;
  letter-spacing: 0.5px;
  font-size: 0.7rem;
  text-align: center;
  cursor: pointer;
}
</style>
