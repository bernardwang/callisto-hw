<template>
  <section class="u-page splash">
    <div class="quote">
      <h3>
        "why are you questioning the victim here? let's flip it. let's talk about what the predator is doing."
      </h3>
    </div>
    <div class="title">
      <h1>
        Tech to Combat Sexual Assult
      </h1>
      <h2>
        We are stronger. Together.
      </h2>
      <button>
        Learn more
      </button>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HomeSplash'
}
</script>

<style scoped lang="scss">
.splash {
  width: 100vw;
  min-height: 45rem;
  background-image: url('~@/assets/person_background.png'), url('~@/assets/faces_background.png');
  background-size: contain, cover;
  background-repeat: no-repeat;
  background-position: 25% 100%, center;
  color: white;
}
.quote {
  padding-top: 10rem;
  margin-left: 50vw;
  width: 18rem;
}
.title {
  margin-top: 10rem;
  width: 25rem;
}
</style>
