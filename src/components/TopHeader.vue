<template>
  <header>
    <div class="logo">
      <img :src="require('@/assets/logo.svg')"/>
    </div>
    <div class="burger"></div>
  </header>
</template>

<script>
export default {
  name: 'TopHeader',
}
</script>

<style scoped>
  header {
    padding: 16px 7%;
    display: flex;
    flex-direction: row;
    gap: 24px;
    align-items: center;
    border-bottom: 1px solid rgba(0,0,0,.1);
    justify-content: space-between;
  }
  .burger {
    width: 25px;
    height: 25px;
    background-image: url("@/assets/burger.svg");
    cursor: pointer;
    background-position: center;
    background-size: cover;
  }
</style>
