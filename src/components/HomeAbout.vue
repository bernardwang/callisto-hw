<template>
  <section class="u-page about">
    <div class="who">
      <h2>
        Who we are
      </h2>
      <p>
        "Callisto is a non-profit organization that develops technology to combat sexual assault and harassment. Our technology is designed to empower survivors with options to seek support and identify repeat perpetrators. Callisto Campus is our flagship online system, which enables student survivors to document and report sexual assault and help identify repeat perpetrators."
      </p>
      <button>
        Learn more
      </button>
    </div>
    <div class="what">
      <h2>
        "What we do"
      </h2>
      <p>
        Callisto's platform provides victims with trauma sensitive options for reporting sexual assault and harrassment. Currently in place across 13 partner campuses, Callisto is expanding in 2018 to serve professional industries.
      </p>
      <button>
        Learn more
      </button>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HomeAbout'
}
</script>

<style scoped lang="scss">
.about {
  min-height: 40rem;
  background-color: white;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  margin: 2rem;
}
.who {
  width: 40%;
  padding-top: 5rem;
}
.what {
  width: 40%;
  padding-top: 20rem;
}
</style>
