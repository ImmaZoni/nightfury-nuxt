<template>
  <div>
    <img :src="author.img">
    <div>
      <h4>Author</h4>
      <p>{{ author.name }}</p>
      <p>{{ author.bio }}</p>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    author: {
      type: Object,
      required: true
    }
  }
}
</script>
<style>
.author-wrap {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  background-color: #f1f1f1;
}
.author-img {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  border: 1px solid #e0e0e0;
  margin: 10px;
}
.author-name {
  font-size: 20px;
  font-weight: bold;
  margin: 10px;
}
.author-bio {
  font-size: 16px;
  margin: 10px;
}
</style>
