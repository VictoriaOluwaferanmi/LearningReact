// Conditional Rendering Directives (v-if,v-else, v-else-if v-show)

<script>
export default {
  name: "App",
  data() {
    return {
      names: ["Vic", "Ayo", "Tayo"],
      fullNames: [
        { first: "Victoria", last: "Ayeni" },
        { first: "Anthony", last: "Ayeni" },
      ],
    };
  },
};
</script>

<template>
  <div>
    <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>

    <h2 v-for="name in fullNames" :key="name.first">
      {{ name.first }} {{ name.last }}
    </h2>
  </div>
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
