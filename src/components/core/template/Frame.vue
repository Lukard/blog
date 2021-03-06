<template>
  <div class="frame">
    <Menu />
    <slot v-if="title == null" />
    <div class="content" v-else>
      <h1 class="title">{{ title }}</h1>
      <slot />
    </div>
  </div>
</template>

<script>
import Menu from '../organism/Menu';
export default {
  name: 'Frame',
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
  display: flex;
  flex-direction: row;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  color: #1c2834;
}
.title {
  margin-left: 16px;
}
.content {
  overflow: auto;
}
@media only screen and (max-width: 768px) {
  .frame {
    flex-direction: column;
  }
}
</style>
