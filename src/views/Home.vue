<template>
  <div class="flex-center">
    <div class="home-content">
      <img :src="getImgUrl('logo')" />
      <h1>100 days of ui challenge</h1>
      Siin on repo, kuhu panna enda UI-harjutused. Kasuta Vue routerit ja route,
      et ülesandeid eraldada. Css võib olla inline, scss ja sass on kasutatavad,
      lessi saab ka sisse lülitada (kes tahab).
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {},
  data() {
    return {
      imgsrc: "logo",
    };
  },
  methods: {
    getImgUrl(img) {
      var images = require.context("../assets/", false, /\.png$/);
      return images("./" + img + ".png");
    },
  },
};
</script>

<style lang="scss">
.flex-center {
  display: flex;
  justify-content: center;
}
.home {
  &-content {
    max-width: 50vh;
    min-width: 400px;
  }
}
</style>
