<template>
  <header class="bar">
    <li class="item">
      <ul class="item">
        <div class="course-container">
          <DartIcon />
          <h1 class="course-name">Dart course</h1>
        </div>
      </ul>
    </li>
  </header>
</template>

<script>
import DartIcon from "../atom/DartIcon.vue";
export default {
  name: "CourseBar",
  components: {
    DartIcon,
  },
};
</script>

<style scoped>
.bar {
  display: flex;
}
.item {
  list-style-type: none;
  margin: 0;
  padding-inline: 0;
}
.course-container {
  margin: 16px;
  padding: 8px 32px;
  background-color: #1C2834;
  border-radius: 64px;
  display: flex;
  align-items: center;
}
.course-name {
  margin-left: 16px;
  color: white;
}
</style>