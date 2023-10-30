<template>
  <div>
    <div>
      <el-input placeholder="Student name" v-model="input" clearable style="width: 200px;">
      </el-input>
      <el-button type="warning" style="margin-left: 5px;">Search</el-button>
    </div>

    <div>
      <el-table :data="tableData" style="width: 100%">
        <el-table-column prop="date" label="Date" width="180">
        </el-table-column>
        <el-table-column prop="name" label="Name" width="180">
        </el-table-column>
        <el-table-column prop="address" label="Address">
        </el-table-column>
        <el-table-column prop="command" label="Command">
          <el-button type="primary">Modify</el-button>
          <el-button type="danger">Delete</el-button>
        </el-table-column>
      </el-table>
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      input: '', 
      tableData: [{
        date: '2016-05-02',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1518 弄'
      }, {
        date: '2016-05-04',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1517 弄'
      }, {
        date: '2016-05-01',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1519 弄'
      }, {
        date: '2016-05-03',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1516 弄'
      }
    ]}
  }

}
</script>

