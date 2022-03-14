<template>
  <FrontNav />
  <router-view />
</template>

<script>
import FrontNav from '@/components/FrontNav.vue'

export default ({
  name: 'HomeView',
  components: {
    FrontNav
  }
})
</script>
