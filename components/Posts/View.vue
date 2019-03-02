<template>
  <section class="out">
    <div class="feed-card in">
      <div class="post-title">{{title}}</div>
      <div class="post-date"></div>
      <div class="post-info">
        <span class="post-creator">k220j</span>
        <span class="post-view"> 12,3000 </span>
        <span class="post-share">400 </span>
      </div>
      <div class="post-image">
        <img :src="imageUrl"
             width="90%"
        />
      </div>
      <div class="content">
        {{content}}
      </div>
      <div class="container">
      </div>
    </div>
  </section>
</template>

<script>
  import axios from 'axios'
  export default {
    props: {
      id: { type: Number, required: true }, // 콘텐츠 id
      title: { type: String, required: true }, // 콘텐츠 타이틀
      content: { type: String, required: true }, // 콘텐츠 내용
      imageUrl: { type: String, require: true }, // 콘텐츠 썸네일
      created_at: { type: String, require: true }, // 콘텐츠 썸네일
    },
  }
</script>

<style scoped>
  .out {
    width: 100%;
    text-align: center;
    margin-top: 1em;
  }

  .in {
    display: inline-block;
  }

  .feed-card {
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    transition: 0.3s;
    width: 90%;
    border-radius: 5px;
    text-align: center;
  }

  img {
    border-radius: 5px 5px 0 0;
  }

  .container {
    padding: 2px 16px;
  }
</style>
