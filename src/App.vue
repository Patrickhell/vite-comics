<template>
  <div>
    <AppHeader />
    <AppMain />
    <AppFooter />
    
  </div>
  
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: 'ComicsApp',
  components:{
    AppHeader,
    AppMain,
    AppFooter,
  }
}
</script>

<style lang="scss">
@import './styles/general.scss'

</style>