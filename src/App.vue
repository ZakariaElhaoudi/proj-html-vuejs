<script>
import PageFooter from './components/PageFooter.vue'
import PageHeader from './components/PageHeader.vue'
import PageMain from './components/PageMain.vue'
export default {
  name: 'App',
  components: {
    PageHeader,
    PageFooter,
    PageMain,

  },
}
</script>

<template>
  <PageHeader />
  <PageMain />
  <PageFooter />
</template>

<style lang="scss">
@use './styles/partials/mixins.scss' as *;
@use './styles/general.scss' as *;
@use './styles/partials/variables.scss' as *;
</style>
