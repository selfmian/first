<template>
  <div>
    <el-row class="tac">
      <el-col :span="6">
        <el-menu
          active-text-color="#ffd04b"
          background-color="#545c64"
          class="el-menu-vertical-demo"
          default-active="1"
          text-color="#fff"
          @open="handleOpen"
          @close="handleClose"
          width="200px"
        >
          <el-menu-item index="1">
            <el-icon><icon-menu /></el-icon>
            <span>首页</span>
          </el-menu-item>
          <el-sub-menu index="2">
            <template #title>
              <el-icon><location /></el-icon>
              <span>菜单</span>
            </template>
            <el-menu-item-group title="菜单1">
              <el-menu-item index="1-2">菜单1-2</el-menu-item>
            </el-menu-item-group>
            <el-menu-item-group title="菜单2"> </el-menu-item-group>
          </el-sub-menu>
          <el-menu-item index="3">
            <el-icon><document /></el-icon>
            <span>图标</span>
          </el-menu-item>
        </el-menu>
      </el-col>
    </el-row>
  </div>
</template>

<script lang="ts">
export default {
  name: "Home",
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
el-menu {
  width: 200px;
  height: 100vh;
}
</style>