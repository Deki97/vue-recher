<template>
  <div id="app">

    <Header />

    <Banner />

    <Activities />

    <CompanyHistory />

    <News />

    <PreFooter />

    <Footer />

  </div>
</template>

<script>
import Header from './components/Header.vue'
import Banner from './components/Banner.vue'
import Activities from './components/Activities.vue'
import CompanyHistory from './components/CompanyHistory.vue'
import News from './components/News.vue'
import PreFooter from './components/PreFooter.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Banner,
    Activities,
    CompanyHistory,
    News,
    PreFooter,
    Footer
  }
}
</script>

<style lang="scss">
@import './style/general.scss';
@import './style/mixins.scss';


</style>
