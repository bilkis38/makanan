<template>
  <div class="home">
    <NavbarWa />
    <div class="container">
      <HeroWa />
    </div>    
  </div>
</template>

<script>
// @ is an alias to /src
import NavbarWa from '@/components/NavbarWa.vue'
import HeroWa from '@/components/HeroWa.vue'

export default {
  name: 'HomeView',
  components: {
    NavbarWa,
    HeroWa
  }
}
</script>
