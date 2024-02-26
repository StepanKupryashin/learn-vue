<script setup>
import { RouterLink, RouterView } from 'vue-router'
import links from "../src/utils/links"
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <RouterLink v-for="link in links" :key="link.name" :to=link.to>{{ link.name }}</RouterLink>
        <!-- <button @click="incriment">count : {{ count }}</button> -->
      </nav>
    </div>
  </header>

  <RouterView />

  <footer>

  </footer>
</template>

<style scoped>
  header {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    background: hsla(160, 100%, 37%, 1);
    height: max-content;
  }

  nav {
    color: black;
  }

  a {
    color: black;
  }

  footer {
    background: rgba(1, 55, 36, 0.651);
    width: 100%;
    height: 15vh;
    position: relative;
    bottom: 0;
  }
</style>

<script>
export default {
  data() {
    return {
      msg: "jghjkgh",
      count: 0,

    }
  },
  methods: {
    incriment() {
      this.count++
    }
  }
}
</script>