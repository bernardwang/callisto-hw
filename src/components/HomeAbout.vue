<template>
  <section class="u-page about typography">
    <div class="section who">
      <h2 class="title">
        Who we are
      </h2>
      <p class="desc">
        Callisto is a non-profit organization that develops technology to combat sexual assault and harassment. Our technology is designed to empower survivors with options to seek support and identify repeat perpetrators. Callisto Campus is our flagship online system, which enables student survivors to document and report sexual assault and help identify repeat perpetrators.
      </p>
      <button class="btn">
        Learn more
      </button>
    </div>
    <div class="section what">
      <h2 class="title">
        What we do
      </h2>
      <p class="desc">
        Callisto's platform provides victims with trauma sensitive options for reporting sexual assault and harrassment. Currently in place across 13 partner campuses, Callisto is expanding in 2018 to serve professional industries.
      </p>
      <button class="btn">
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
@import '@/styles/_color.scss';

.about {
  min-height: 40rem;
  background-color: $cl-white;
  position: relative;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: flex-start;
  margin-left: 4rem;
  margin-right: 4rem;

  &:before {
    content: "";
    position: absolute;
    border-left: 1px solid $cl-text-secondary;
    top: -4rem;
    left: 45%;
    height: 20rem;
  }
  &:after {
    content: "";
    position: absolute;
    border-left: 1px solid $cl-text-secondary;
    bottom: 0rem;
    right: 44%;
    height: 25rem;
  }
}
.section {
  position: relative;
  z-index: 1;
  &:before {
    position: absolute;
    z-index: -1;
    left: -2rem;
    bottom: -3rem;
    font-size: 10rem;
    font-weight: bold;
    color: rgba(200,200,200,0.5);
  }
}
.who {
  padding-top: 3rem;
  width: 40%;
  &:before {
    content: "01";
  }
}
.what {
  padding-top: 15rem;
  width: 45%;
  &:before {
    content: "02";
  }
}
.title {
}
.desc {
  padding-left: 3rem;
}
.btn {
  float: right;
  margin-top: 1rem;
}
</style>
