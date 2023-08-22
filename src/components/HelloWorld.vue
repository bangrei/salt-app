<template>
  <div class="hello">
    <top-header></top-header>
    <div class="main">
      <top-banner></top-banner>
      <div class="content">
        <slide-content></slide-content>
        <core-values></core-values>
        <our-specialty></our-specialty>
      </div>
    </div>
    <main-footer></main-footer>
  </div>
</template>

<script>
import TopHeader from './TopHeader.vue';
import TopBanner from './TopBanner.vue';
import SlideContent from './SlideContent.vue';
import CoreValues from './CoreValues.vue';
import OurSpecialty from './OurSpecialty.vue';
import MainFooter from './MainFooter.vue';
export default {
  name: 'HelloWorld',
  components: {
    TopHeader,
    TopBanner,
    SlideContent,
    CoreValues,
    OurSpecialty,
    MainFooter
  }
}
</script>

<style scoped>
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
</style>
