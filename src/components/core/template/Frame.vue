<template>
  <div id="app" class="frame">
    <Menu />
    <slot v-if="title == null" />
    <div v-else>
      <h1 class="title">{{ title }}</h1>
      <slot />
    </div>
  </div>
</template>

<script>
import Menu from "../organism/Menu";
export default {
  name: "Frame",
  components: {
    Menu,
  },
  props: {
    title: String,
  },
};
</script>

<style scoped>
.frame {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: row;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #1C2834;
  height: 100%;
}
.title {
  margin-left: 16px;
}
@media only screen and (max-width: 768px) {
  .frame {
    flex-direction: column;
  }
}
</style>