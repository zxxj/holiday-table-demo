<script setup>
const holiday = [
  '1月21日(除夕)',
  '1月22日(初一)',
  '1月23日(初二)',
  '1月24日(初三)',
  '1月25日(初四)',
  '1月26日(初五)',
  '1月27日(初六)',
];

const tableData = [
  {
    enterprise: '凯新公司', //企业名称
    person: '刘善祥', // 联系人
    phone: '13803367800', // 联系电话
    days: 7, // 放假天数
    work: 8, // 工作天数
    one: 1, // '1月21日(除夕)'
    two: 2, // '1月22日(初一)
    three: 3, // '1月23日(初二)'
    four: 4, // '1月24日(初三)'
    five: 5, // '1月25日(初四)'
    six: 6, // '1月26日(初五)'
    seven: 7, // '1月27日(初六)'
    notes: '备注信息',
  },
  {
    enterprise: '众城通信',
    person: '张绪芳',
    phone: '18631136814',
    days: 10,
    work: 6,
    one: 11,
    two: 22,
    three: 33,
    four: 44,
    five: 55,
    six: 66,
    seven: 77,
    notes: '备注信息',
  },
];
</script>

<template>
  <div class="table-contaier">
    <div class="key column">序号</div>
    <div class="name column">企业名称</div>
    <div class="person column">紧急联系人</div>
    <div class="phone column">联系电话</div>
    <div class="days column">放假天数</div>
    <div class="work column">上班天数</div>
    <div class="holiday">
      <div class="top">进入园区人数</div>
      <div class="bottom">
        <div class="item" v-for="item in holiday">
          <div class="date">{{ item }}</div>
        </div>
      </div>
    </div>
    <div class="work column">备注</div>
  </div>

  <el-table
    :data="tableData"
    style="width: 100%"
    type="index"
    :show-header="false"
  >
    <el-table-column type="index" width="50" align="center"></el-table-column>
    <el-table-column prop="enterprise" width="130" align="center">
    </el-table-column>
    <el-table-column prop="person" width="130" align="center">
    </el-table-column>
    <el-table-column prop="phone" width="130" align="center"> </el-table-column>
    <el-table-column prop="days" width="130" align="center"> </el-table-column>
    <el-table-column prop="work" width="130" align="center"> </el-table-column>
    <!-- <el-table-column prop="one" width="140" align="center"></el-table-column>
    <el-table-column prop="two" width="140" align="center"></el-table-column>
    <el-table-column prop="three" width="140" align="center"></el-table-column>
    <el-table-column prop="four" width="140" align="center"></el-table-column>
    <el-table-column prop="five" width="140" align="center"></el-table-column>
    <el-table-column prop="six" width="140" align="center"></el-table-column>
    <el-table-column prop="seven" width="140" align="center"></el-table-column> -->

    <template v-for="item in holiday">
      <el-table-column>
        <!-- {{ item }} -->
        1
      </el-table-column>
    </template>
    <el-table-column prop="notes" width="130"> </el-table-column>
  </el-table>
</template>

<style scoped>
.table-contaier {
  width: 100%;
  display: flex;
  background-color: #f2f2f2;
  height: 100px;
  text-align: center;
  font-weight: bold;
  .key {
    width: 50px !important;
  }

  .column {
    width: 130px;
    border: 1px solid orange;
    border-collapse: collapse;
    margin: 0 0 -1px -1px;
    line-height: 100px;
  }

  .holiday {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    .top {
      display: flex;
      align-items: center;
      justify-content: center;
      border: 1px solid red;
      height: 50%;
      margin: 0 0 -1px -1px;
    }
    .bottom {
      display: flex;
      height: 50%;
      .item {
        padding: 0 20px;
        border: 1px solid red;
        margin: 0 0 -1px -1px;
      }
    }
  }
}
</style>
