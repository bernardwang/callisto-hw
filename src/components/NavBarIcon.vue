<template>
  <div @click="onClick" :class="iconClass">
    <span></span>
    <span></span>
    <span></span>
  </div>
</template>

<script>
export default {
  name: 'HamburgerMenu',
  props: [ 'open', 'onClick' ],
  computed: {
    iconClass: function () {
      return {
        'icon': true,
        'icon-open': this.open
      }
    }
  }
}
</script>

<style scoped lang="scss">
@import '@/styles/_variables.scss';

.icon {
  display: none;
  width: 2.75rem;
  height: 2rem;
  position: absolute;
  top: 2.5rem;
  right: 3rem;
  z-index: 3;

  transform: rotate(0deg);
  transition: .5s ease-in-out;
  cursor: pointer;
}

.icon span {
  display: block;
  position: absolute;
  height: 0.25rem;
  width: 100%;
  background: $cl-white;
  border-radius: 0.5rem;
  opacity: 1;
  left: 0;
  transform: rotate(0deg);
  transition: .25s ease-in-out;

  &:nth-child(1){
    top: 0rem;
    transform-origin: left center;
  }
  &:nth-child(2){
    top: 1rem;
    transform-origin: left center;
  }
  &:nth-child(3){
    top: 2rem;
    transform-origin: left center;
  }
}

.icon-open span {
  &:nth-child(1){
    transform: rotate(45deg);
    top: 0.25rem;
    left: 0.4rem;
  }
  &:nth-child(2){
    width: 0%;
    opacity: 0;
  }
  &:nth-child(3){
    transform: rotate(-45deg);
    top: 2.25rem;
    left: 0.4rem;
  }
}
</style>
