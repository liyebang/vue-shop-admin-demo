<template>
    <el-menu
      default-active="1-1"
      class="el-menu-vertical-demo"
      @open="handleOpen"
      @close="handleClose"
      background-color="#001529"
      text-color="#fff"
      active-text-color="#ffd04b"
      :collapse="isCollapse">
      <el-submenu index="1">
        <template slot="title">
          <i class="el-icon-menu"></i>
          <span>购物商城</span>
        </template>
        <el-menu-item index="1-1">
          <router-link to="/admin/goods-list">商品管理</router-link>
        </el-menu-item>
        <el-menu-item index="1-2">
          <router-link to="/admin/category-list">栏目管理</router-link>
        </el-menu-item>
      </el-submenu>

      <!-- <el-menu-item index="2">
        <i class="el-icon-menu"></i>
        <span slot="title">导航二</span>
      </el-menu-item> -->
      
     
    </el-menu>

</template>


<script>
  export default {
    methods: {
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    },
    props:['isCollapse']
  }
</script>

<style scoped>
  .el-menu-vertical-demo{
    height: 100%;
  }
  .el-menu-vertical-demo:not(.el-menu--collapse) {
    width: 200px;
    min-height: 400px;
  }
  .el-menu-vertical-demo a{
    color: inherit;
    text-decoration: none
  }
</style>
