<template>
  <div>

<el-container style="height: 500px; border: 1px solid #eee">
  <el-aside width="200px" style="background-color: rgb(238, 241, 246)">
    <el-menu :default-openeds="['3']" router inique-opened :default-active="$route.path">
      <el-submenu index="1">
        <template slot="title"><i class="el-icon-message"></i>内容管理</template>
       <el-menu-item-group>
          <template slot="title">物品</template>
          <el-menu-item index="/items/add">新建物品</el-menu-item>
          <el-menu-item index="/items/list"> 物品列表</el-menu-item>
        </el-menu-item-group> 
         <el-menu-item-group>
          <template slot="title">英雄</template>
          <el-menu-item index="/heros/add">新建英雄</el-menu-item>
          <el-menu-item index="/heros/list"> 英雄列表</el-menu-item>
        </el-menu-item-group> 
      <el-menu-item-group>
        <template slot="title">文章</template>
          <el-menu-item index="/articles/add">新建文章</el-menu-item>
          <el-menu-item index="/articles/list"> 文章列表</el-menu-item>
        </el-menu-item-group>
      </el-submenu>
       
       <el-submenu index="2">
          <template slot="title"><i class="el-icon-message"></i>运营管理</template>
         
          <el-menu-item-group>
            <template slot="title">广告</template>
            <el-menu-item index="/ads/add">新建广告位</el-menu-item>
            <el-menu-item index="/ads/list"> 广告位列表</el-menu-item>
          </el-menu-item-group>
       </el-submenu>
        <el-submenu index="3">
            <template slot="title"><i class="el-icon-message"></i>系统设置</template>
            <el-menu-item-group>
              <template slot="title">分类</template>
              <el-menu-item index="/categories/list">分类列表</el-menu-item>
              <el-menu-item index="/categories/createEdit"> 新建分类</el-menu-item>
            </el-menu-item-group>
             <el-menu-item-group>
            <template slot="title">人员管理</template>
            <el-menu-item index="/admin_users/add">新建管理员</el-menu-item>
            <el-menu-item index="/admin_users/list"> 管理员列表</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
       
    </el-menu> 
     
  </el-aside>
  
  <el-container>
     <el-header style="text-align: right; font-size: 12px"></el-header>
     <el-main>
       <router-view :key="$route.path"></router-view>
     </el-main>
  </el-container>
</el-container>
    
  </div>
</template>
<style>
  .el-header {
    background-color: #B3C0D1;
    color: #333;
    line-height: 60px;
  }
  
  .el-aside {
    color: #333;
  }
</style>

<script>
  export default {
    data() {
      const item = {
        date: '2016-05-02',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1518 弄'
      };
      return {
        tableData: Array(20).fill(item)
      }
    }
  };
</script>