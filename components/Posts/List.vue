<template>
  <section class="outer">
    <div class="inner">
      <nuxt-link :to="`/posts/${id}`" class="">
        <img
          :src="imageUrl"
          class="thumbnail"
        />
        <div class="centered">
          <div class="card-header"></div>
          <div class="post-title"><H3>{{ title }}</H3></div>
          <div class="post-info">
            <span class="post-creator">k220j</span>
            <span class="post-view">조회수 {{20400}}</span>
          </div>
        </div>
      </nuxt-link>
    </div>
  </section>
</template>
<script>
  export default {
    props: {
      id: {type: Number, required: true}, // 콘텐츠 id
      title: {type: String, required: true}, // 콘텐츠 타이틀
      content: {type: String, required: true}, // 콘텐츠 내용
      imageUrl: {type: String, require: true}, // 콘텐츠 썸네일
    },
  }
</script>

<style lnag="sass" scoped>
  $primary-color:red;
  .outer {
    display: table;
    width: 98%;
    padding:1rem;
    height: 100%;
    background-color: $primary-color;
  }

  .inner {
    display: table-cell;
    vertical-align: middle;
    text-align: center;
  }

  .centered {
    position: relative;
    display: inline-block;
  }

  .post-title {
    position: relative;
  }

  .post-info {
    margin-top: 1rem;
  }

  .thumbnail {
    width: 100%;
    height: auto;
    max-width: 300rem;
    max-height: 40vh;
  }

  a {
    color: black
  }
</style>
