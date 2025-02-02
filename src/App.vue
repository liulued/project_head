<template>
  <div id="app">
    <router-view/>
    <el-container>
      <el-header style="background-color: #687179">
        <img src="@/assets/logo.png" alt="" style="width: 40px; position: relative; top: 10px;">
        <span style="font-size: 20px; margin-left: 15px; color: white">校园招聘系统</span>
      </el-header>
    </el-container>

    <el-container>
      <el-aside style="overflow: hidden; min-height: 100vh; background-color: #545c64; width: 250px">
        <el-menu :default-active="$route.path" router background-color="#545c64" text-color="#fff" active-text-color="#ffd04b">
          <el-menu-item index="/home">
            <i class="el-icon-s-home"></i>
            <span slot="title">系统首页</span>
          </el-menu-item>
          <el-submenu index="/person">
            <template slot="title">
              <i class="el-icon-location"></i><span>用户信息管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="/boss">招聘者信息</el-menu-item>
              <el-menu-item index="/user">求职者信息</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
          <el-submenu index="3">
            <template slot="title">
              <i class="el-icon-location"></i><span>信息管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="3-1">xxx信息</el-menu-item>
              <el-menu-item index="3-2">yyy信息</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
        </el-menu>
      </el-aside>
      <el-main>
        <div style="font-size: 12px">这里是主体内容</div>
      </el-main>
    </el-container>
  </div>
</template>

<style>
.el-menu{
  border-right: none !important;
}
</style>


