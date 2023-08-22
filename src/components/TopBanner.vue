<template>
  <div class="banner-wrapper">
    <img :src="require('@/assets/banner.png')" />
    <div class="two">
      <div class="title">
        <span>Discover</span>
        <span>Your wonder</span>
      </div>
      <div class="subtitle">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TopBanner',
}
</script>

<style scoped>
  .banner-wrapper {
    width: 100%;
    background: white;
    position: relative;
  }
  .banner-wrapper img {
    width: 100%;
    max-height: 400px;
  }
  .two {
    position: relative;
    width: 100%;
    height: 250px;
    top: 0px;
    background: #4097DB;
  }
  .two * {
    z-index: 3;
    position: relative;
    background: #4097DB;
  }
  .two:before {
    content: "";
    position: absolute;
    left: -10%;
    right: 0;
    bottom: 0;
    height: 180px;
    background: #4097DB;
    top: -12px;
    transform: rotate(8deg);
    width: calc(100% + 100%);
    z-index: 2;
  }
  .two:after {
    content: "";
    position: absolute;
    left: -10%;
    right: 0;
    bottom: 0;
    height: 120px;
    background: #53A7E9;
    top: -50px;
    transform: rotate(-8deg);
    width: calc(100% + 100%);
    z-index: 1;
  }
  .title {
    color: #FFF;
    font-weight: bold;
    font-size: 2em;
    display: flex;
    flex-direction: column;
    gap: 0px;
    justify-content: flex-start;
    text-align: left;
    padding: 32px 7%;
  }
  .subtitle {
    display: block;
    font-size: 1.1em;
    color: #FFF;
    padding: 32px 7%;
    padding-top: 0;
    text-align: left;
  }
</style>
