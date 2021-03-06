<template>
  <Frame title="Dart variables">
    <div class="lesson-wrapper">
      <h2>What is a variable?</h2>
      <p>
        A variable is used to store information to be referenced and manipulated
        by a computer program. It has the following structure:
      </p>
      <div class="illustration">
        <VariableExampleIllustration />
      </div>
      <h2>Variable types</h2>
      <p>
        First of all, when declaring a variable a <b>type</b> needs to be
        specified. Dart has a specific set of built-in types:
      </p>
      <div class="horizontal-list">
        <div class="type-item">
          <h3>int</h3>
          <p>Integers numbers</p>
          <p>
            <span class="type">int </span><span class="name">counter </span
            ><span class="assignment">= </span> 10;
          </p>
        </div>
      </div>
      <div class="grid">
        <h3><span class="grid-title">Type</span></h3>
        <h3><span class="grid-title">Description</span></h3>
        <h3><span class="grid-title">Example</span></h3>
        <div class="grid-type">int</div>
        <div class="grid-description">Integers numbers</div>
        <div class="grid-example grid-top-right-border">
          <span class="type">int </span><span class="name">counter </span
          ><span class="assignment">= </span> 10;
        </div>
        <div class="grid-type">double</div>
        <div class="grid-description">
          (double precision) Floating-point numbers
        </div>
        <div class="grid-example">
          <span class="type">double </span><span class="name">quarter </span
          ><span class="assignment">= </span> 0.25;
        </div>
        <div class="grid-type">num</div>
        <div class="grid-description">
          Generic number representation. int and double are subtypes of num
        </div>
        <div class="grid-example">
          <span class="type">num </span><span class="name">index </span
          ><span class="assignment">= </span> -1;
        </div>
        <div class="grid-type">String</div>
        <div class="grid-description">Sequence of characters</div>
        <div class="grid-example">
          <span class="type">String </span><span class="name">name </span
          ><span class="assignment">= </span> 'Rubén';
        </div>
        <div class="grid-type">Boolean</div>
        <div class="grid-description">
          Representation of true or false state
        </div>
        <div class="grid-example">
          <span class="type">Boolean </span><span class="name">isEmpty </span
          ><span class="assignment">= </span> true;
        </div>
        <div class="grid-type">List</div>
        <div class="grid-description">Array of items of any type</div>
        <div class="grid-example">
          <span class="type">List&lt;int> </span
          ><span class="name">numbers </span
          ><span class="assignment">= </span> [1, 2, 3];
        </div>
        <div class="grid-type">Set</div>
        <div class="grid-description">Unordered collection of unique items</div>
        <div class="grid-example">
          <span class="type">Set&lt;String> </span
          ><span class="name">technologies </span
          ><span class="assignment">= </span> {'Android', 'iOS', 'Web'};
        </div>
        <div class="grid-type grid-bottom-left-border">Map</div>
        <div class="grid-description">
          collection of values identified by key of given type
        </div>
        <div class="grid-example grid-bottom-right-border">
          <span class="type">Map&lt;String, int> </span
          ><span class="name">colors </span
          ><span class="assignment">= </span> {'red': 0xff0000, 'green':
          0x00ff00, 'blue': 0x0000ff};
        </div>
      </div>

      <h3>Number</h3>
      <p>Dart provide number types through the two following types:</p>
      <h4>int</h4>
      <p>It represents an <b>integer number</b>.</p>
      <div class="code-wrapper">
        <span class="example"><b>Example</b></span>
        <div class="code">
          <span class="type"><b>int </b></span>
          <span class="name">counter</span> <span class="assignment">=</span> 0;
        </div>
      </div>
      <div class="pro-tip">
        <div class="title"><ProTipIcon /><b class="title-text">Pro tip</b></div>
        <div>
          Integer values no longer than 64 bits rely on platform specific
          implementation. On Dart VM, values can be from -2⁶³ to 2⁶³ - 1. But
          when Dart is compiled to Javascript,
          <a
            href="https://stackoverflow.com/questions/2802957/number-of-bits-in-javascript-numbers/2803010#2803010"
          >
            Javascript numbers
          </a>
          is used. It allows values from -2⁵³ to 2⁵³-1.
        </div>
      </div>
      <h4>double</h4>
      <p>
        It represents <b>64-bit (double precision) floating-point numbers</b>,
        as specified by the IEEE 754 standard.
      </p>
    </div>
  </Frame>
</template>

<script>
import Frame from '../../../../core/template/Frame.vue';
import VariableExampleIllustration from '../atom/VariableExampleIllustration.vue';
import ProTipIcon from '../../../../core/atom/ProTipIcon.vue';
export default {
  name: 'DartVariables',
  components: {
    Frame,
    VariableExampleIllustration,
    ProTipIcon,
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
h2 {
  margin: 0;
}
h3 {
  margin-bottom: 8px;
}
h4 {
  margin: 0;
}
.code-wrapper {
  width: 100%;
  margin-top: 16px;
}
.code {
  background-color: #1c2834;
  color: white;
  padding: 16px;
  border-radius: 0px 8px 8px 8px;
  font-family: Consolas, Arial, sans-serif;
  font-size: large;
  width: calc(100% - 32px);
}
.example {
  padding: 16px 16px 4px 16px;
  background-color: #1c2834;
  color: lightgray;
  border-radius: 8px 8px 0px 0px;
}
.type {
  color: greenyellow;
}
.name {
  color: turquoise;
}
.assignment {
  color: pink;
}
.pro-tip {
  padding: 16px;
  background-color: lightyellow;
  border-radius: 16px;
  border-style: solid;
  border-color: darkgoldenrod;
  margin-top: 16px;
  margin-bottom: 16px;
}
.grid {
  display: grid;
  grid-template-columns: 100px 515px auto;
  width: 100%;
  margin-bottom: 16px;
}
.grid-title {
  background-color: #1c2834;
  color: lightgray;
  padding: 16px;
  border-radius: 8px 8px;
}
.grid-type {
  background-color: #1c2834;
  color: greenyellow;
  font-family: Consolas, Arial, sans-serif;
  font-weight: bold;
  font-size: large;
  padding: 8px 16px;
}
.grid-description {
  background-color: #1c2834;
  color: lightgray;
  padding: 8px 16px;
}
.grid-example {
  background-color: #1c2834;
  padding: 8px 16px;
  color: lightgray;
  font-family: Consolas, Arial, sans-serif;
}
.grid-top-right-border {
  border-top-right-radius: 8px;
}
.grid-bottom-right-border {
  border-bottom-right-radius: 8px;
}
.grid-bottom-left-border {
  border-bottom-left-radius: 8px;
}
.horizontal-list {
  display: flex;
  flex-direction: row;
}
.type-item {
  display: flex;
  flex-direction: column;
  background-color: #1c2834;
  color: lightgray;
}
</style>
