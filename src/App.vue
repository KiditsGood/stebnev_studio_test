<template>
  <Header />
  <main class="wrapper">
    <Crumbs :crumbs-items="['Главная', 'Гибрид']" :current-page="'СКАП 252 СВ'" />
    <div class="container">
      <ProductCard />
      <ProductTabs />
    </div>
  </main>
</template>

<script>
  import Header from "@/components/header/Header";
  import Crumbs from "@/components/crumbs/Crumbs";
  import ProductCard from "@/components/productcard/ProductCard";
  import ProductTabs from "@/components/producttabs/ProductTabs";
  export default {
    components: {ProductTabs, ProductCard, Crumbs, Header}
  }
</script>

<style lang="scss">
  @import 'assets/styles/style';
</style>