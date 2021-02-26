<template>
  <Frame title="Dart variables">
    <div class="lesson-wrapper">
      <h2>What is a variable?</h2>
      <p>
        A variable is used to store information to be referenced and manipulated
        by a computer program.
      </p>
      <div>
        <span class="type font-xxlarge">String </span>
        <span class="name font-xxlarge">name </span>
        <span class="assignment font-xxlarge">= </span>
        <span class="value font-xxlarge">'Rubén'</span>
        <span class="terminator font-xxlarge">;</span>
      </div>
    </div>
  </Frame>
</template>

<script>
import Frame from "../../../core/template/Frame.vue";
export default {
  name: "DartVariables",
  components: {
    Frame,
  },
};
</script>

<style scoped>
.lesson-wrapper {
  display: flex;
  flex-direction: column;
  padding: 16px;
  align-items: flex-start;
}
.font-xxlarge {
  font-size: xx-large;
}
.type {
  color: #bf4848;
}
.name {
  color: #983048;
}
.assignment {
  color: #8B2848;
}
.value {
  color: #6B1548;
}
.terminator {
  color: #480048;
}
</style>