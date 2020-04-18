<template>
  <div id="app">
      <h1> Focus !</h1>
      <search-bar />
        <timer />
  </div>
</template>

<script>
import SearchBar from "@/components/SearchBar";
import Timer from "@/components/Timer";

export default {
  name: "App",
  components: {
    SearchBar,
      Timer,
  }

}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

:root {}
</style>
