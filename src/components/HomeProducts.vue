<template>
  <section class="u-page products typography">
    <h2 class="title">
      Our Products
    </h2>
    <div class="card-container">
      <div class="card campus">
        <h5 class="label">
          Flagship
        </h5>
        <h3 class="name">
          Callisto <span class="u-normal"> Campus </span>
        </h3>
        <p class="desc">
          Designed to detect repeat perpertrators and to empower victims to make the reporting decision that feels right for them.
        </p>
        <p class="desc">
          Features include:
        </p>
        <p class="feat">
          Secure encrypted incident reports <br/>
          Option to enroll in Matching system <br/>
          Direct reporting to your institution <br/>
          Support services and local resources
        </p>
        <hr class="divider"/>
        <Button class="button" variant="accent">
          More about Callisto Campus
        </Button>
      </div>
      <div class="card campus">
        <h5 class="label">
          New
        </h5>
        <h3 class="name">
          Callisto <span class="u-normal"> Expansion </span>
        </h3>
        <p class="desc">
          In this version of Callisto, we are adapting our signature matching system to empower victims beyond college campuses:
        </p>
        <p class="desc">
          Features include:
        </p>
        <p class="feat">
          Secure encrypted Matching records <br/>
          Option to create incident reports <br/>
          Access to a Callisto Options Counselor (if Matched) <br/>
          Support services and local resources
        </p>
        <hr class="divider"/>
        <Button class="button" variant="accent">
          More about Callisto Expansion
        </Button>
      </div>
    </div>
  </section>
</template>

<script>
import Button from '@/components/core/Button'

export default {
  name: 'HomeProducts',
  components: { Button }
}
</script>

<style scoped lang="scss">
@import '@/styles/_variables.scss';

.products {
  padding-top: 1rem;
  padding-bottom: 3rem;
  min-height: 30rem;
  background-color: $cl-bg-dark;
}
.title {
  width: 100%;
  text-align: center;
  color: $cl-text-secondary;
}
.card-container {
  width: 100%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
}
.card {
  position:relative;
  margin: 1rem;
  padding: 2rem 3rem 2rem 3rem;
  width: 100%;
  max-width: 23rem;
  background-color: $cl-white;
  border-radius: 2px;
  text-align: center;
  @include breakpoint(medium) {
    margin: 1rem 0 1rem 0;
  }
}
.label {
  text-transform: uppercase;
  letter-spacing: 1px;
  margin: 0;
}
.name {
  margin-top: 1rem;
}
.desc {
  font-weight: 500;
}
.feat {
  margin-top: 2rem;
  line-height: 2;
}
.divider {
  border: 0.5px solid #ddd;
  position: absolute;
  width: 95%;
  left: 2.5%;
  bottom: 6rem;
}
.button {
  width: 100%;
  margin-top: 2rem;
  padding-top: 1rem;
  padding-bottom: 1rem;
  border-radius: 3px;
}
</style>
