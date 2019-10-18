<template>
  <d2-container>
    <template slot='header'>Page 2 header</template>
    <div>
      <el-row :gutter='20'>
        <el-col :span='8'>
          <el-card shadow='hover' class='card'>
            <i class='el-icon-s-custom custom' />
          </el-card>
        </el-col>
        <el-col :span='8'>
          <number-card icon='el-icon-s-custom' title='测试' color='red'/>
        </el-col>
        <el-col :span='8'>
          <el-card shadow='hover'>
            <i class='el-icon-s-custom custom' />
          </el-card>
        </el-col>
      </el-row>
    </div>
  </d2-container>
</template>

<script>
import numberCard from '../components/number-card'
export default {
  name: 'users',
  components: {
    numberCard
  }
}
</script>

<style>
.el-row {
  margin-bottom: 20px;
}
.el-col {
  border-radius: 4px;
}
.card {
  padding: 24px 36px 24px 0px;
}
.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
.custom {
  padding: 10px;
  color: darkorange;
  width: 70px;
  height: 70px;
}
</style>
