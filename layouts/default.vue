<template>
  <el-container>

    <el-header>
      <AppHeader />
    </el-header>

    <el-main>
      <nuxt />
    </el-main>

    <el-footer />

  </el-container>
</template>

<script>
import AppHeader from '@/components/client/AppHeader.vue'

export default {
  components: {
    AppHeader
  }
}
</script>