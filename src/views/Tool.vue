<template>
  <el-card class="box-card">
    <div slot="header" class="clearfix">
      <span>卡片名称</span>
      <!-- <el-button style="float: right; padding: 3px 0" type="text">操作按钮</el-button> -->
    </div>
    <div v-for="o in 4" :key="o" class="text item">
      {{ "列表内容 " + o }}
    </div>
    <el-button type="text" @click="table = true"
      >打开嵌套表格的 Drawer</el-button
    >
    <el-drawer
      title="我嵌套了表格!"
      :visible.sync="table"
      direction="rtl"
      size="50%"
    >
      <iframe
        src="https://tool.lu/timestamp"
        class="iframe"
      >
      </iframe>
    </el-drawer>
  </el-card>
</template>

<script>
export default {
    data(){
        return {
            table: false
        }
    }
};
</script>

<style scoped>
.iframe{
    border-top-width: 0px;
    border-right-width: 0px;
    border-bottom-width: 0px;
    border-left-width: 0px;
    width: 100%;
    height: 100%;
}
.text {
  font-size: 14px;
}

.item {
  margin-bottom: 18px;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}
.clearfix:after {
  clear: both;
}

.box-card {
  width: 30%;
}
</style>