<template>
  <div id="app">
    <Header />
    <p>
      JAVASCRIPT TEXT: <span class="red">{{ text }}</span>
    </p>
    <p>
      <button @click="hello">Say Hello</button>
    </p>
    <router-link to="/">Home</router-link><br><br>
    <router-link to="about">About</router-link>
    <router-view />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  components: {
    Header,
    Footer,
  },
  data() {
    return {
      text: "This is some text",
    };
  },
  methods: {
    hello() {
      alert("Hello World!");
    },
  },
};
</script>

<style>
.red {
  color: red;
}
</style>