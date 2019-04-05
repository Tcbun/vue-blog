<template>
  <div class="blogRightHome">
    <dl v-for="item in items" :key="item.id">
      <dt>
        <h2>{{item.newsTitle}}</h2>
      </dt>
      <dd>
        <router-link to="/">{{item.newsDesc}}</router-link>
        <span>{{item.newsDate}}</span>
      </dd>
    </dl>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "blogRightHome",
  components: {},
  data() {
    return {
      items: []
    };
  },
  methods: {
    getArticle() {
      axios
        .get(
          "https://www.easy-mock.com/mock/5ca31b5f6e33f32c06ac3c97/example/qiansongke"
        )
        .then(this.reqSucc);
    },
    reqSucc(res) {
      // console.log(res)
      this.items = res.data.items;
    }
  },
  mounted() {
    this.getArticle();
  }
};
</script>

<style lang="scss" scoped>
.blogRightHome {
  width: 100%;
  padding-left: 40px;
  padding-top: 88px;
  background: #f5f5f5;
  dl {
    margin-bottom: 50px;
    dt {
      h2 {
        font-weight: normal;
        font-size: 22px;
        margin-bottom: 16px;
      }
    }
    dd {
      list-style-type: disc;
      position: relative;
      a {
        color: #000;
        text-decoration: underline;
        margin-right: 100px;
        letter-spacing: 2px;
      }
      a:hover {
        color: #f4606c;
      }
      a::before {
        content: "";
        width: 5px;
        height: 21px;
        background: #f4606c;
        position: absolute;
        left: -10px;
      }
    }
  }
}
</style>
