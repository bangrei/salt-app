<template>
    <div class="items">
      <div class="item" v-for="(item, i) in items" :key="i">
        <div class="item-title">{{ item.title }}</div>
        <div class="item-subtitle">{{ item.subtitle }}</div>
        <div class="item-text">{{ item.text }}</div>
        <div class="item-actions">
            <div class="item-action-number">
                <div class="item-number-current">{{ i+1 < 10 ? 0 : ''}}{{ i+1 }}</div>
                <div class="item-number-separator">/</div>
                <div class="item-number-page">{{ items.length < 10 ? 0 : ''}}{{ items.length }}</div>
            </div>
            <div class="item-action-nav">
                <div class="item-nav-prev"></div>
                <div class="item-nav-next"></div>
            </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'SlideContent',
  data() {
    return {
        items: []
    }
  },
  created() {
    this.items = [
        {
            id: 1,
            title: 'Who we are',
            subtitle: 'Technology Company',
            text: 'ed ut perspiciatis unde omnis iste natus sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.',
        },
        {
            id: 2,
            title: 'What we do',
            subtitle: 'Professional Brand Manager',
            text: 'ed ut perspiciatis unde omnis iste natus sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.',
        },
        {
            id: 3,
            title: 'How we do',
            subtitle: 'Strategize, Design, Collaborate',
            text: 'ed ut perspiciatis unde omnis iste natus sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.',
        },
    ]
  }
}
</script>

<style scoped>
  .items {
    padding-top: 48px;
    display: flex;
    align-items: center;
    gap: 24px;
    overflow: hidden;
    overflow-x: scroll;
  }
  .item {
    padding: 24px 7%;
    width: 100%;
    max-width: 400px;
    min-width: 300px;
    display: flex;
    flex-direction: column;
  }
  .item-title {
    color: #029FE4;
    font-size: 36px;
    font-style: normal;
    font-weight: 500;
    line-height: 30px; /* 83.333% */
  }
  .item-title + * {
    padding-top: 24px;
  }
  .item-subtitle {
    color: #000;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 38px; /* 211.111% */
  }
  .item-text {
    color: #777;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 24px; /* 171.429% */
    letter-spacing: 0.14px;
  }
  .item-actions {
    display: flex;
    justify-content: space-between;
    gap: 24px;
    padding-top: 48px;
  }
  .item-action-number {
    display: flex;
    align-items: center;
    gap: 2px;
  }
  .item-number-current {
    color: #303030;
    font-size: 24px;
    font-style: normal;
    font-weight: 500;
    line-height: 38px; /* 158.333% */
  }
  .item-number-separator {
    color: #C0C0C0;
    font-size: 24px;
    font-style: normal;
    font-weight: 500;
    line-height: 38px;

  }
  .item-number-page {
    color: #C0C0C0;
    font-size: 16px;
    font-style: normal;
    font-weight: 500;
    line-height: 38px;
  }
  .item-action-nav {
    display: flex;
    align-items: center;
    gap: 0px;
    cursor: pointer;
  }
  .item-nav-prev {
    background-image: url("@/assets/nav.svg");
    width: 50px;
    height: 50px;
    background-position-x: left;
  }
  .item-nav-next {
    background-image: url("@/assets/nav.svg");
    width: 50px;
    height: 50px;
    background-position-x: right;
  }
</style>
