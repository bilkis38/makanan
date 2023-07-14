<template>
  <div class="FoodsView">
    <NavbarWa />
    <h1>Daftar Makanan</h1>
  </div>
</template>

<script>
// @ is an alias to /src
import NavbarWa from '@/components/NavbarWa.vue'

export default {
  name: 'FoodsView',
  components: {
    NavbarWa
  }
}
</script>