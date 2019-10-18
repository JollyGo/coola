<template>
  <d2-container>
    <template slot="header">Page 2 header</template>
    <div>
      <el-row :gutter="20">
        <el-col :span="6">
          <div class="grid-content bg-purple"></div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple"></div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple"></div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple"></div>
        </el-col>
      </el-row>
    </div>
  </d2-container>
</template>

<script>
export default {
  name: 'page2'
}
</script>

<style>
.el-row {
  margin-bottom: 20px;
}
.el-col {
  border-radius: 4px;
}
.bg-purple-dark {
  background: #99a9bf;
}
.bg-purple {
  background: #f1f3f5;
}
.bg-purple-light {
  background: #ebf1f6;
}
.grid-content {
  border-radius: 4px;
  min-height: 7rem;
}
.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
</style>
