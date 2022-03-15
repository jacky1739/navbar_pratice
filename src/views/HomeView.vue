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
    alert () {
      console.log('click Father layer')
    }
  },
  mounted () {
    emitter.on('click', () => {
      this.alert()
    })
  }
})
</script>
