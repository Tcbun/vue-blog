<template>
  <div class="blog-sidebar">
    <div class="blog-sidebar-title">
      <p>钱松科的个人博客</p>
    </div>
    <div class="blog-icon-wrap">
      <div class="blog-icon">
        <img src="../../assets/icon.jpg" alt>
      </div>
    </div>
    <div class="blog-tag-list">
      <ul>
        <li>
          <span class="iconfont iconhome"></span>
          <router-link to="/" class="active-now">首页</router-link>
        </li>
        <li>
          <span class="iconfont icontype"></span>
          <router-link to="/">分类</router-link>
        </li>
        <li>
          <span class="iconfont icontag"></span>
          <router-link to="/">标签</router-link>
        </li>
        <li>
          <span class="iconfont iconpeople"></span>
          <router-link to="/">关于</router-link>
        </li>
        <li>
          <span class="iconfont iconmore"></span>
          <router-link to="/">更多</router-link>
        </li>
      </ul>
    </div>
    <div class="copyright">
      <p>钱松科vue-blog作品</p>
      <p>CopyRight@2019</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.active-now {
  border-bottom: 2px solid #fff;
}
.blog-sidebar {
  position: relative;
  width: 250px;
  height: 100%;
  background: #202020;
  padding-top: 100px;
  .blog-sidebar-title {
    color: #fff;
    text-align: center;
    margin-bottom: 30px;
  }
  .blog-icon-wrap {
    width: 160px;
    padding-top: 5px;
    margin: 0 auto;
    background: #fff;
    .blog-icon {
      width: 150px;
      margin: 0 auto;
      overflow: hidden;
      img {
        width: 100%;
      }
    }
  }
  .blog-tag-list {
    color: #fff;
    text-align: center;
    margin-top: 50px;
    ul li {
      margin-bottom: 36px;
      span {
        margin-right: 15px;
      }
      a {
        padding-bottom: 10px;
      }
      a:hover {
        font-size: 18px;
        border-bottom: 2px solid #F4606C;
        transition: all 0.5s;
      }
    }
  }
  .copyright {
    position: absolute;
    color: #fff;
    text-align: center;
    font-size: 12px;
    bottom: 50px;
    left: 50%;
    margin-left: -55.92px;
  }
}
</style>
