<template>
  <section class="u-page splash" id="splash">
    <NavBar />
    <div class="article-container">
      <aside class="article quote" role="complementary">
        <p class="quote-text headline">
          'why are you questioning the victim here? let's flip it. let's talk about what the predator is doing.'
        </p>
      </aside>
      <article class="article intro">
        <h1 class="intro-display">
          Tech to Combat Sexual Assault
        </h1>
        <p class="intro-headline">
          We are stronger. Together.
        </p>
        <Button variant="primary">
          Learn more
        </Button>
      </article>
    </div>
    <button @click="scrollToAbout" class="scroll">
      <p class="scroll-text">
        Scroll down
      </p>
    </button>
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
  },
  methods: {
    scrollToAbout: function () {
      const aboutSection = document.querySelector('#about')
      if (aboutSection) {
        aboutSection.scrollIntoView({alignToTop: true, behavior: 'smooth' })
      }
    }
  }
}
</script>

<style scoped lang="scss">
@import '@/styles/_variables.scss';

.splash {
  position: relative;
  min-height: 100vh;
  background-image: url('~@/assets/person_background.png'), url('~@/assets/faces_background.png');
  background-size: contain, cover;
  background-repeat: no-repeat;
  background-position: 25% 100%, center;
  color: $cl-white;
  overflow-x: hidden;
  @include breakpoint(medium) {
    // TODO: find better responsive solution for quote
    .quote {
      width: 100%;
    }

    // Remove lines and scroll
    // TODO: find better responsive solution for line visual elements
    .quote-text:before {
      border: none;
    }

    .scroll-text {
      transform: rotate(0deg);
    }
  }
}
.article-container {
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  align-items: flex-end;
}
.quote {
  width: 35%;
  margin-top: 8rem;
}
.intro {
  width: 100%;
  margin-bottom: 4rem;
}
.intro-display {
  max-width: 30rem;
  font-family: $playfair-stack;
  font-weight: 900;
  margin: 0;
  margin-bottom: 1.5rem;
}
.intro-headline {
  font-family: $oswald-stack;
  font-weight: 500;
  font-size: 2rem;
  margin-top: 1.5rem;
}
.quote-text {
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
    right: -9rem;
    width: 10rem;
  }
}
.scroll {
  position: absolute;
  border: 0;
  background: transparent;
  width: 3rem;
  left: 41%;
  bottom: 1rem;
  transition: transform $time-normal;
  &:hover, &:focus {
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
  color: $cl-white;
}
</style>
