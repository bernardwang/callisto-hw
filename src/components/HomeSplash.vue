<template>
  <section class="u-page splash">
    <div class="title">
      <h1>
        Tech to Combat Sexual Assult
      </h1>
      <h3>
        We are stronger. Together.
      </h3>
      <button>
        Learn more
      </button>
    </div>
    <div class="quote">
      <h3>
        "why are you questioning the victim here? let's flip it. let's talk about what the predator is doing."
      </h3>
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
.splash {
  min-height: 40rem;
  background-image: url('~@/assets/person_background.png'), url('~@/assets/faces_background.png');
  background-size: contain, cover;
  background-repeat: no-repeat;
  background-position: 25% 100%, center;
  color: white;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
}
.quote {
  width: 30%;
  padding-top: 15rem;
}
.title {
  width: 40%;
  margin-top: 25rem;
}
</style>
