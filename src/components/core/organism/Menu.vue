<template>
  <div class="menu">
    <img
      class="profile-image"
      src="../../../assets/profile.jpg"
      alt="Rubén Abad picture"
    />
    <h1 class="profile-name">Rubén Abad Sánchez</h1>
    <p class="profile-text">
      I work as <b>Senior Android Developer</b> at <b>New Work S.E.</b> (a.k.a.
      <b>Xing</b>). This is my personal blog and all thoughts and knowledge
      shared here are mine, and mine alone.
    </p>
    <p class="profile-text">
      I'm really interested in <b>Android</b> and
      <b>Flutter/Dart</b> development. The content of this blog is related with
      this awesome technologies.
    </p>
    <SocialBar />
  </div>
</template>

<script>
import SocialBar from "../molecule/SocialBar.vue";
export default {
  name: "Menu",
  components: {
    SocialBar,
  },
};
</script>

<style scoped>
.menu {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  max-width: 400px;
  padding: 16px;
  background-image: linear-gradient(#32de84, #42a5f5);
}
.profile-image {
  border-radius: 50%;
  width: 200px;
  box-shadow: 0px 0px 0px 8px #fff;
  padding: 4px;
}
.profile-name {
  color: white;
}
.profile-text {
  text-align: left;
  color: white;
}
@media only screen and (max-width: 768px) {
  .menu {
    max-width: 100%;
    background-image: linear-gradient(0.25turn, #32de84, #42a5f5);
  }
  .profile-image {
    width: 100px;
    box-shadow: 0px 0px 0px 4px #fff;
  }
}
</style>