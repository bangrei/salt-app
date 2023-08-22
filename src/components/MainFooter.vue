<template>
  <footer>
    <div class="logo">
      <img :src="require('@/assets/footer.svg')"/>
    </div>
    <div class="box">
        <div class="box-dropdown">
            <div class="box-dropdown-selected" @click="showItems = !showItems">
                <span>{{ selectedItem }}</span>
                <span class="caret"></span>
            </div>
            <div class="box-dropdown-items" v-if="showItems">
                <div 
                    class="box-dropdown-item" 
                    :class="{'selected': item == selectedItem}"
                    v-for="(item, i) in items" 
                    @click="selectItem(item)"
                    :key="i">{{ item }}</div>
            </div>
        </div>
        <div class="box-address">
            Jl. Lembong No 8 Kel. Braga Kec. Sumur Bandung, Kota Bandung, Jawa Barat
        </div>
    </div>
    <div class="footer-list">
        <div class="footer-list-item" v-for="(it, x) in list" :key="x">{{ it }}</div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'MainFooter',
  data() {
    return {
        items: [],
        showItems: false,
        selectedItem: "Select One",
        list: [],
    }
  },
  methods: {
    selectItem(item) {
        this.selectedItem = item;
        this.showItems = false;
    }
  },
  created() {
    this.items = ["Technologies", "Design", "Feature", "Logic"];
    this.list = ["Who We Are", "Our Values", "Perks"];
  }
}
</script>

<style scoped>
  footer {
    padding: 16px 7%;
    display: flex;
    flex-direction: column;
    gap: 24px;
    align-items: flex-start;
    border-bottom: 1px solid rgba(0,0,0,.1);
    justify-content: space-between;
    background: #07477A;
  }
  .box {
    background: #FFF;
    padding: 16px;
  }
  .box-dropdown {
    display: flex;
    flex-direction: column;
    border: 1px solid rgba(0,0,0,.1);
    padding: 8px 16px;
    border-radius: 4px;
    position: relative;
  }
  .box-dropdown-selected {
    display: flex;
    align-items: center;
    justify-content: space-between;
    cursor: pointer;
  }
  .box-dropdown-items {
    background: #FFF;
    position: absolute;
    display: flex;
    flex-direction: column;
    gap: 12px;
    top: 36px;
    left: 0;
    right: 0;
    border: 1px solid rgba(0,0,0,.1);
    border-radius: 4px;
  }
  .box-dropdown-item {
    cursor: pointer;
    padding: 8px 16px;
  }
  .box-dropdown-item + .box-dropdown-item {
    padding-top: 0 !important;
  }
  .box-dropdown-item:hover {
    background: #25A0D8;
    color: #FFF;
  }
  .caret {
    width: 15px;
    height: 15px;
    background-image: url("@/assets/caret-down.svg");
    background-position: center;
    background-size: cover;
  }
  .box-address {
    padding-top: 16px;
    color: #25A0D8;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
    letter-spacing: 0.36px;
  }
  .footer-list {
    display: flex;
    flex-direction: column;
    gap: 32px;
    color: #FFF;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
  }
</style>
