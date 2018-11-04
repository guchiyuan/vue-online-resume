<template>
  <div class="resume">
    <el-container>
      <el-aside class="menu-panel" width="300px">
        <el-menu mode="verticle" collapse="false" default-active="1-4-1" class="el-menu-vertical-demo" @open="handleOpen" @close="handleClose">
          <el-submenu index="1">
            <template slot="title">
              <i class="el-icon-location"></i>
              <!-- <span slot="title">导航一</span> -->
            </template>
          </el-submenu>
        </el-menu>
      </el-aside>
      <el-main class="content-panel">Main</el-main>
    </el-container>
  </div>
</template> 

<script>


export default {
  name: 'resume',
  components: {
  }
}
</script>

<style lang="stylus" scoped>
  .menu-panel
    margin .3rem
    background-color #eee
    height 600px
  .content-panel
    background-color #666
    margin .3rem
</style>

