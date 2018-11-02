<template>
  <div class="headerview">
    <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
      <el-menu-item index="1">简历制作</el-menu-item>
      <el-menu-item index="2">关于我</el-menu-item>
    </el-menu>
  </div>
</template>

<script>
export default {
  name: 'headerview',
  data() {
    return {
      activeIndex: '2',
    }
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<style lang="stylus" scoped>

</style>


