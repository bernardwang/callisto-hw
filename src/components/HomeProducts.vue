<template>
  <section class="u-page products">
    <h2 class="section-title">
      Our Products
    </h2>
    <div class="product-container">
      <div class="product campus">
        <h4 class="product-label">
          Flagship
        </h4>
        <h3 class="product-name">
          <span class="u-bold"> Callisto </span> Campus
        </h3>
        <p class="product-desc">
          Designed to detect repeat perpertrators and to empower victims to make the reporting decision that feels right for them.
        </p>
        <p class="product-desc">
          Features include:
        </p>
        <p class="product-feat">
          Secure encrypted incident reports <br/>
          Option to enroll in Matching system <br/>
          Direct reporting to your institution <br/>
          Support services and local resources
        </p>
        <hr class="product-divider"/>
        <button class="product-btn">
          More about Callisto Campus
        </button>
      </div>
      <div class="product campus">
        <h4 class="product-label">
          New
        </h4>
        <h3 class="product-name">
          <span class="u-bold"> Callisto </span> Expansion
        </h3>
        <p class="product-desc">
          In this version of Callisto, we are adapting our signature matching system to empower victims beyond college campuses:
        </p>
        <p class="product-desc">
          Features include:
        </p>
        <p class="product-feat">
          Secure encrypted Matching records <br/>
          Option to create incident reports <br/>
          Access to a Callisto Options Counselor (if Matched) <br/>
          Support services and local resources
        </p>
        <hr class="product-divider"/>
        <button class="product-btn">
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
.products {
  min-height: 30rem;
  background-color: gray;
}
.section-title {
  width: 100%;
  text-align: center;
}
.product-container {
  width: 100%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 2rem;
}
.product {
  position:relative;
  margin: 1rem;
  margin-top: 2rem;
  padding: 2rem;
  width: 100%;
  max-width: 30rem;
  background-color: white;
  border-radius: 2px;
  text-align: center;
}
.product-label {
  text-transform: uppercase;
  letter-spacing: 1px;
}
.product-name {

}
.product-desc {

}
.product-feat {

}
.product-divider {
  position: absolute;
  width: 95%;
  left: 2.5%;
  bottom: 4rem;
}
.product-btn {
  margin-top: 2rem;
}
</style>
