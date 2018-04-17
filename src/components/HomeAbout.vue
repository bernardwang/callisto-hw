<template>
  <section class="u-page about" id="about">
    <article class="article who" role="article">
      <h2 class="title">
        Who we are
      </h2>
      <p class="desc">
        Callisto is a non-profit organization that develops technology to combat sexual assault and harassment. Our technology is designed to empower survivors with options to seek support and identify repeat perpetrators. Callisto Campus is our flagship online system, which enables student survivors to document and report sexual assault and help identify repeat perpetrators.
      </p>
      <Button class="button" variant="accent">
        Learn more
      </Button>
    </article>
    <article class="article what" role="article">
      <h2 class="title">
        What we do
      </h2>
      <p class="desc">
        Callisto's platform provides victims with trauma sensitive options for reporting sexual assault and harrassment. Currently in place across 13 partner campuses, Callisto is expanding in 2018 to serve professional industries.
      </p>
      <Button class="button" variant="accent">
        Learn more
      </Button>
    </article>
  </section>
</template>

<script>
import Button from '@/components/core/Button'

export default {
  name: 'HomeAbout',
  components: { Button }
}
</script>

<style scoped lang="scss">
@import '@/styles/_variables.scss';

.about {
  min-height: 35rem;
  margin: 0 2vw 0 2vw;
  padding-bottom: 9rem;
  background-color: $cl-white;
  position: relative;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: flex-start;

  &:before {
    content: "";
    position: absolute;
    border-left: 1px solid $cl-text-secondary;
    top: -4rem;
    left: 46%;
    height: 20rem;
  }
  &:after {
    content: "";
    position: absolute;
    border-left: 1px solid $cl-text-secondary;
    bottom: 0rem;
    right: 45%;
    height: 30rem;
  }
  @include breakpoint(large) {
    margin: 0;
  }
  @include breakpoint(medium) {
    flex-direction: column;

    // Remove lines
    // TODO: find better way to handle responsiveness for visual elements
    &:before, &:after {
      border: none;
    }
  }
}
.who {
  width: 40%;
  padding-top: 3rem;
  &:before {
    content: "01";
  }
}
.what {
  width: 47%;
  padding-top: 19rem;
  .desc {
    padding-left: 5rem;
  }
  &:before {
    content: "02";
  }
}
.article {
  position: relative;
  z-index: 1;
  &:before {
    position: absolute;
    z-index: -1;
    left: -2rem;
    bottom: -3rem;
    font-family: $playfair-stack;
    font-size: 15rem;
    font-weight: 400;
    letter-spacing: 0.3rem;
    color: rgba(#B8A9A3,0.3);
  }
  @include breakpoint(medium) {
    width: 100%;
    padding-top: 2rem;
  }
}
.title {
  font-family: $playfair-stack;
  font-size: 3.5rem;
}
.desc {
  padding-left: 3rem;
}
.button {
  float: right;
  margin-top: 1rem;
}
</style>
