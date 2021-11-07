<template>
  <div class="admin-layout">
    <el-container :style="{height: '100%'}">
      <el-aside width="250px">
        <AppAside />
      </el-aside>
      <el-main>
        <nuxt />
      </el-main>
    </el-container>
  </div>
</template>

<script>
  import AppAside from '@/components/admin/AppAside.vue'
    export default {
      name: "admin",
      components: {AppAside}
    }
</script>

<style lang="scss" scoped>
  .admin-layout{
    width: 100%;
    height: 100vh;
  }
</style>
