//
<script>
export default {
  name: "SingleComponent1",
  data() {
    return {
      name: `<b> Victoria </b>`,
      age: 24,
      channel: "Evolution",
      hack: `<a href="#" onClick="alert('You have been hacked!')"> Win a prize! <a/>`,
      title: "This is the title",
      headingId: "heading",
      isDisabled: true,
      status: "danger",
      pStyleObject: {
        color: "blue",
        fontSize: 50 + "px",
      },
    };
  },
};
</script>

<template>
  <header>
    <div>
      <h1 v-html="name"></h1>
      <p :style="pStyleObject">Using color from string data</p>
      <h1 class="underline">I am {{ age }} years</h1>
      <div v-html="hack"></div>
      <div v-bind:title="title">Hover over me to see the title</div>
      <h2 v-bind:id="headingId">Heading</h2>
      <button v-bind:disabled="isDisabled">My Button</button>
      <h2 v-bind:class="status">Status</h2>
    </div>
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
