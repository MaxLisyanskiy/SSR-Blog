<template>
  <article class="post">
    <header class="post-header">
      <div class="post-title">
        <h1>Post</h1>
        <nuxt-link to="/">
          <i class="el-icon-back"></i>
        </nuxt-link>
      </div>
      <div class="post-info">
        <small>
          <i class="el-icon-time"></i>
          {{ new Date().toLocaleString() }}
        </small>
        <small>
          <i class="el-icon-view"></i>
          <span>42</span>
        </small>
      </div>
      <div class="post-img">
        <img src="https://nuts-agency.ru/upload/iblock/c98/c9879095ed083e4a3076480c3573b87f.png" alt="">
      </div>
    </header>
    <main class="post-content">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et, velit.
    </main>
    <footer class="post-footer">

      <AppCommentForm/>

      <div class="comments" v-if="true">
        <AppComment
          v-for="comment in 4"
          :key="comment"
          :comment="comment"
        />
      </div>
      <div class="text-center" v-else>
        Комментариев нет
      </div>


    </footer>
  </article>
</template>

<script>
import AppComment from '~/components/client/AppComment'
import AppCommentForm from '~/components/client/AppCommentForm'

export default {

  validate({params}) {
    return Boolean(params.id)
  },
  components: {
    AppComment, AppCommentForm
  }
}
</script>

<style lang="scss" scoped>
  .post{
    max-width: 600px;
    margin: 0 auto;

    &-header{
      margin-bottom: 2rem;
    }

    &-title {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 1rem;
    }

    &-info {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: .5rem;
    }

    &-img {
      img {
        width: 100%;
        height: auto;
      }
    }

    &-content{
      margin-bottom: 2rem;
    }
  }
</style>
