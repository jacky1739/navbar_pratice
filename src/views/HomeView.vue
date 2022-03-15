<template>
  <FrontNav :click="alert"></FrontNav>
  <router-view />
</template>

<script>
import FrontNav from '@/components/FrontNav.vue'
import emitter from '@/assets/javascript/emitter'

export default ({
  name: 'HomeView',
  components: {
    FrontNav
  },
  methods: {
    alert (item) {
      console.log('click Father layer', item)
    }
  },
  mounted () {
    emitter.on('click', (item) => {
      this.alert(item)
    })
  }
})
</script>
