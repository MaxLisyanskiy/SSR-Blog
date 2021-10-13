<template>
  <el-card
    shadow="hover"
    :body-style="{padding: 0}"
    class="post"
  >
    <header slot="header" class="post-header">
      <h3>post</h3>
      <small>
        <i class="el-icon-time"></i>
        {{ new Date().toLocaleString() }}
      </small>
    </header>

    <div class="post-body">
      <img 
        src="" 
        alt="" 
        class="post-img"
      >
    </div>
    <footer class="post-footer">
      <el-button round @click="openPost">Открыть</el-button>
      <span>
        <i class="el-icon-chat-dot-round"></i>
        <span>12</span>
      </span>
    </footer>
  </el-card>
</template>

<script>
export default {
  methods: {
    openPost() {
      const id = '123'
      this.$router.push(`/post/${id}`)
    }
  }
}
</script>

<style lang="scss" scoped>
  .post {
    margin-bottom: 25px;

    &-img {
      width: 100%;
      height: auto;
    }
    &-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem;
    }
  }
</style>