<script>
import AppFooter from './components/AppFooter.vue'
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
export default {
  name: 'App',
  components: {
    AppHeader,
    AppFooter,
    AppMain,

  },
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
@use './styles/partials/mixins.scss' as *;
@use './styles/general.scss' as *;
@use './styles/partials/variables.scss' as *;
</style>
