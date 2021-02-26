<template>
  <div class="grid">
    <router-link :to="{ name: 'DartVariables' }">
      <div class="item">
        <VariablesIllustration />
        <div class="content">
          <h2 class="title">Variables in Dart</h2>
          <p>
            Let's dig into the basics of Dart. We are going to learn how to
            declare and initialize variables, study the available types and
            check which modifiers can be use
          </p>
          <div class="date">February 20, 2021</div>
        </div>
      </div>
    </router-link>
    <div></div>
    <div></div>
  </div>
</template>

<script>
import VariablesIllustration from "../atom/VariablesIllustration.vue";
export default {
  name: "CourseGrid",
  components: {
    VariablesIllustration,
  },
};
</script>

<style scoped>
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 3fr));
  grid-gap: 16px;
  padding: 16px;
}
.item {
  background-color: #1C2834;
  color: white;
  border-top-left-radius: 32px;
  border-top-right-radius: 32px;
  border-bottom-left-radius: 16px;
  border-bottom-right-radius: 16px;
  display: flex;
  flex-direction: column;
  cursor: pointer;
}
.item:hover {
  box-shadow: 0px 0px 8px 4px rgba(28, 40, 52, 0.5);
}
.content {
  padding: 16px;
  text-align: left;
  display: flex;
  flex-direction: column;
}
.title {
  margin: 0;
}
.date {
  text-align: right;
}
a {
  text-decoration: inherit;
  color: inherit;
}
</style>