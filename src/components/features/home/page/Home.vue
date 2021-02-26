<template>
  <Frame>
    <div>
      <CourseBar />
      <main>
        <CourseGrid />
      </main>
      <footer></footer>
    </div>
  </Frame>
</template>

<script>
import Frame from "../../../core/template/Frame.vue";
import CourseBar from "../organism/CourseBar.vue";
import CourseGrid from "../organism/CourseGrid.vue";
export default {
  name: "Home",
  components: {
    Frame,
    CourseBar,
    CourseGrid,
  },
};
</script>