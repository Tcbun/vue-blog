<template>
  <div class="wrap">
    <blog-side-bar></blog-side-bar>
    <blog-right-home></blog-right-home>
  </div>
</template>

<script>
import blogSideBar from "../components/home/blogSideBar.vue";
import blogRightHome from "../components/home/blogRightHome.vue";
export default {
  name:'Home',
  components: {
    blogSideBar,
    blogRightHome
  }
};
</script>

<style lang="scss">
.wrap {
  width: 100%;
  height: 100%;
  display: flex;
}
</style>
