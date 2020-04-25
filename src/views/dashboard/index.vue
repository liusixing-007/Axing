<template>
  <div class="dashboard-container">
    <div class="dashboard-text">欢迎：{{ name }}</div>
    <div class="dashboard-text">角色：<span v-for="role in roles" :key="role">{{ role }}</span></div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'Dashboard',
  computed: {
    ...mapGetters([
      'name',
      'roles'
    ])
  }
}
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
.dashboard {
  &-container {
    margin: 100px;
  }
  &-text {
    font-size: 50px;
    line-height: 50px;
  }
}
</style>
