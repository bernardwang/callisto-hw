<template>
  <router-link v-if="to" v-bind:to="to">
    <button :class="classObj">
      <slot></slot>
    </button>
  </router-link>
  <button v-else :class="classObj">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: [ 'variant', 'to' ],
  computed: {
    classObj: function () {
      return {
        'button': true,
        'variant-primary': this.variant === 'primary',
        'variant-secondary': this.variant === 'secondary',
        'variant-accent': this.variant === 'accent'
      }
    }
  }
}
</script>

<style scoped lang="scss">
@import '@/styles/_variables.scss';

.button {
  padding: 0.8rem 2.5rem 0.8rem 2.5rem;
  border: none;
  font-weight: 500;
  font-size: 1rem;
  cursor: pointer;
  transition: background $time-fast, color $time-fast;
}
.variant-primary {
  background-color: $cl-white;
  color: $cl-text-primary;
  &:hover {
    @extend .variant-accent
  }
}
.variant-secondary {
  background-color: $cl-bg-dark;
  color: $cl-white;
  &:hover {
    @extend .variant-accent
  }
}
.variant-accent {
  background-color: $cl-text-accent;
  color: $cl-white;
  &:hover {
    @extend .variant-secondary
  }
}
</style>
