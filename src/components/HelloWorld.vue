<template>
  <div class="hello">
    <el-checkbox-group v-model="checkList" :min="1" :max="2">
    <el-checkbox :label="1">复选框 A</el-checkbox>
    <el-checkbox :label="2">复选框 B</el-checkbox>
    <el-checkbox :label="3">复选框 C</el-checkbox>
    <el-checkbox :label="4" disabled>禁用</el-checkbox>
    <el-checkbox :label="5" disabled>选中且禁用</el-checkbox>
  </el-checkbox-group>

  <el-table
    :data="tableData6"
    border
    height="600"
    
    show-summary
    style="width: 100%; margin-top: 20px">
    <el-table-column
      type="index"
      :render-header="ran"
      :index="indexMethod">

    </el-table-column>
    <el-table-column
      prop="id"
      label="ID"
      :render-header="ren"
      width="180">
    </el-table-column>
    <el-table-column
      prop="name"
      label="姓名">
    </el-table-column>
    <el-table-column
      prop="amount1"
      label="数值 1（元）">
    </el-table-column>
    <el-table-column
      prop="amount2"
      label="数值 2（元）">
    </el-table-column>
    <el-table-column
      prop="amount3"
      label="数值 3（元）">
    </el-table-column>
  </el-table>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      checkList: [1, 5, 3],
      tableData6: [
        {
          id: "12987122",
          name: "王小虎",
          amount1: "234",
          amount2: "3.2",
          amount3: 10
        },
        {
          id: "12987123",
          name: "王小虎",
          amount1: "165",
          amount2: "4.43",
          amount3: 12
        },
        {
          id: "12987124",
          name: "王小虎",
          amount1: "324",
          amount2: "1.9",
          amount3: 9
        },
        {
          id: "12987125",
          name: "王小虎",
          amount1: "621",
          amount2: "2.2",
          amount3: 17
        },
        {
          id: "12987126",
          name: "王小虎",
          amount1: "539",
          amount2: "4.1",
          amount3: 15
        }
      ]
    };
  },
  methods: {
    indexMethod(index) {
      return index + 1;
    },
    ren(h, { column, $index }) {
      return h("div", {}, column.label);
    },
    ran(h, { column, $index }) {
      console.log($index);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
