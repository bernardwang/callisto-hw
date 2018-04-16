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
        <button class="btn">
          More about Callisto Campus
        </button>
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
        <button class="btn">
          More about Callisto Expansion
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HomeProducts'
}
</script>

<style scoped lang="scss">
@import '@/styles/_color.scss';

.products {
  padding: 4rem;
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
  margin-top: 2rem;
  padding: 2rem;
  width: 100%;
  max-width: 25rem;
  background-color: $cl-white;
  border-radius: 2px;
  text-align: center;
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
  line-height: 2;
}
.divider {
  position: absolute;
  width: 95%;
  left: 2.5%;
  bottom: 4rem;
}
.btn {
  margin-top: 2rem;
}
</style>
