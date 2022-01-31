<template>
  <div id="app">
    <Header />
    <div class="container">
      <router-view />
    </div>
    <div class="footer">
      <MyFooter />
    </div>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import MyFooter from "@/components/MyFooter.vue";

export default {
  components: {
    Header,
    MyFooter,
  },
};
</script>

<style>
.container {
  max-width: 1400 px;
  margin: 0 auto;
}
.footer {
  width: 100%;
  background: #222;
  margin-top: 159px;
}
</style>
