// Conditional Rendering Directives (v-if,v-else, v-else-if v-show) //

<script>
export default {
  name: "App",
  data() {
    return {
      num: 2,
      display: true,
      showElement: true,
    };
  },
};
</script>

<template>
  <header>
    <h2 v-if="num === 0">number is zero</h2>
    <h2 v-else-if="num > 0">The number is positive</h2>
    <h2 v-else-if="num < 0">The number is negative</h2>
    <h2 v-else>The is not a number</h2>
    <template v-if="display">
      <h2>Victoria</h2>
      <h2>Oluwaferanmi</h2>
      <h2>Ayeni</h2>
    </template>
    <h2 v-show="showElement">Using vshow</h2>
    <h2 v-if="showElement">Using vshow</h2>
  </header>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
.underline {
  text-decoration: underline;
}
</style>
