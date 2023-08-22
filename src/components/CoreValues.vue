<template>
  <div class="core-wrapper">
    <div class="core-title">Our Core Values</div>
    <div class="core-desc">Ridiculus laoreet libero pretium et, sit vel elementum convallis fames. Sit suspendisse etiam eget egestas. Aliquet odio et lectus etiam sit. In mauris rutrum ac ut volutpat, ornare nibh diam. Montes, vitae, nec amet enim.</div>
    <div class="core-list">
        <div class="core-list-item" v-for="(item, i) in items" :key="i">
            <div class="core-list-item-label">{{ item.label }}</div>
            <div class="core-list-item-text">{{ item.text }}</div>
        </div>
    </div>
    <div class="core-image">
        <img :src="require('@/assets/core-values.png')" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'CoreValues',
  data() {
    return {
        items: [],
    }
  },
  created() {
    this.items = [
        {
            id: 1,
            label: "Dedication",
            text: "Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat.",
        },
        {
            id: 2,
            label: "Intellectual Honesty",
            text: "Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias conse.",
        },
        {
            id: 3,
            label: "Curiosity",
            text: "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque.",
        },
    ]
  }
}
</script>

<style scoped>
  .core-wrapper {
    padding: 32px 7%;
  }
  .core-title {
    color: #029FE4;
    font-size: 36px;
    font-style: normal;
    font-weight: 500;
    line-height: 30px; /* 83.333% */
  }
  .core-title + * {
    padding-top: 24px;
  }
  .core-desc {
    color: #777;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 24px; /* 150% */
    letter-spacing: 0.16px;
  }
  .core-list {
    display: flex;
    flex-direction: column;
    gap: 24px;
    padding-top: 24px;
  }
  .core-list-item {
    display: flex;
    flex-direction: column;
    gap: 6px;
  }
  .core-list-item-label {
    position: relative;
    padding-left: 40px;
    display: flex;
    width: 257px;
    height: 38px;
    flex-direction: column;
    justify-content: center;
    flex-shrink: 0;
    color: #000;
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 38px; /* 158.333% */
  }
  .core-list-item-label::before {
    content: "";
    width: 25px;
    height: 2px;
    background: #000;
    position: absolute;
    left: 0;
  }
  .core-list-item-text {
    padding-left: 40px;
  }
  .core-image {
    padding: 16px 0;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .core-image img {
    width: 100%;
    max-width: 400px;
    margin: auto;
  }
</style>
