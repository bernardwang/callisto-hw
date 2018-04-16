<template>
  <main>
    <HomeSplash/>
    <HomeAbout/>
    <HomeProducts/>
  </main>
</template>

<script>
import HomeSplash from '@/components/HomeSplash'
import HomeAbout from '@/components/HomeAbout'
import HomeProducts from '@/components/HomeProducts'

export default {
  name: 'Home',
  components: {
    HomeSplash,
    HomeAbout,
    HomeProducts
  }
}
</script>

<style scoped lang="scss">
</style>
