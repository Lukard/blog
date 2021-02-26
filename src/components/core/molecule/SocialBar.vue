<template>
  <div>
    <a href="https://twitter.com/Shichiro"><TwitterIcon /></a>
    <a href="https://github.com/Lukard"><GithubIcon /></a>
    <a href="https://www.linkedin.com/in/rubenabadsanchez/">
      <LinkedInIcon />
    </a>
  </div>
</template>

<script>
import TwitterIcon from "../atom/TwitterIcon.vue";
import GithubIcon from "../atom/GithubIcon.vue";
import LinkedInIcon from "../atom/LinkedInIcon.vue";
export default {
  name: "SocialBar",
  components: {
    TwitterIcon,
    GithubIcon,
    LinkedInIcon,
  },
};
</script>

<style scoped>
div {
  display: flex;
}
a {
  max-width: 56px;
  max-height: 56px;
  cursor: pointer;
  margin-right: 16px;
  margin-left: 16px;
  margin-top: 32px;
}
@media only screen and (max-width: 768px) {
  div {
    display: flex;
    justify-content: flex-end;
  }
  a {
    max-width: 48px;
    max-height: 48px;
    cursor: pointer;
    margin: 16px;
  }
}
</style>