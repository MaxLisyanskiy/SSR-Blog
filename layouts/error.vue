<template>
  <div class="error-layout">
    <div class="error-content">
      <h1 class="error-title">404</h1>
      <nuxt-link to='/' class="error-btn">Вернуться на главную</nuxt-link>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .error-layout{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
  }

  .error-content{
    margin-top: 100px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .error-title{
    font-size: 200px;
    color: rgb(4, 138, 22);
    margin-bottom: 30px;
  }

  .error-btn{
    text-decoration: none;
    color: black;
    border: 1px solid rgb(119, 255, 8);
    border-radius: 8px;
    padding: 15px;
  }
</style>