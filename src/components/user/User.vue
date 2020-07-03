<template>
    <div>
        <!-- 面包屑导航区域 -->
        <el-breadcrumb separator-class="el-icon-arrow-right">
            <el-breadcrumb-item :to="{ path: '/Home' }">首页</el-breadcrumb-item>
            <el-breadcrumb-item>用户管理</el-breadcrumb-item>
            <el-breadcrumb-item>用户列表</el-breadcrumb-item>
        </el-breadcrumb>
        <!-- 卡片视图区域 -->
        <el-row :gutter="10">
          <el-col :span="10">
            <el-card class="box-card user" style="height:613px;">
              <div slot="header" class="clearfix">
                <span>个人信息</span>
              </div>
              <div class="user-body">
                <el-row class="user-info">
                <el-col :span="12"><div class="grid-content bg-purple"><i class="el-icon-tickets"></i>  账号：123456 <i class="el-icon-trophy"></i></div></el-col>
                <el-col :span="12"><div class="grid-content bg-purple-light"><i class="el-icon-user"></i>  姓名：admin</div></el-col>
                <el-col :span="12"><div class="grid-content bg-purple"><i class="el-icon-office-building"></i>  公司：胜时代生物科技有限公司</div></el-col>
                <el-col :span="12"><div class="grid-content bg-purple-light"><i class="el-icon-s-operation"></i>  权限：管理员</div></el-col>
                <el-col :span="12"><div class="grid-content bg-purple"><i class="el-icon-phone-outline"></i>  联系电话：13888888888</div></el-col>
                <el-col :span="12"><div class="grid-content bg-purple-light"><i class="el-icon-message"></i>  邮箱：13888888888@qq.com</div></el-col>
                <el-col :span="12"><div class="grid-content bg-purple-light"><i class="el-icon-medal"></i>  积分：100</div></el-col>
                <el-col :span="12"><div class="grid-content bg-purple-light"><i class="el-icon-coin"></i>  澳币：1888</div></el-col>
              </el-row>
              <el-row :gutter="10" class="user-button" type="flex" justify="end" align="bottom">
                <el-col :span="4">
                  <el-button type="primary">修改信息</el-button>
                </el-col>
                <el-col :span="4">
                  <el-button type="success">修改权限</el-button>
                </el-col>
                <el-col :span="4">
                  <el-button type="warning">充值澳币</el-button>
                </el-col>
                <el-col :span="4">
                  <el-button type="danger">充值明细</el-button>
                </el-col>
              </el-row>
              </div>

            </el-card>
          </el-col>
          <el-col :span="14">
            <el-card class="box-card" >
              <div slot="header" class="clearfix">
                <span>任务记录</span>
              </div>
              <!-- <el-table :data="tableData" :column="tableColumn" style="width: 100%" min-height="500px">
                <el-table-column prop="date" label="日期" width="180"></el-table-column>
                <el-table-column prop="name" label="姓名" width="180"></el-table-column>
                <el-table-column prop="address" label="地址"></el-table-column>
              </el-table> -->
              <Table :tableData="tableData" :tableColumns="tableColumn" style="width: 100%" min-height="500px"></Table>
            </el-card>
          </el-col>
        </el-row>
        <el-row>
          <el-col>
            <el-card class="box-card paper">
              <div slot="header" class="clearfix">
                <span>发表论文引用:</span>
              </div>
              <div class="notice">
                <p>
                  如果您在数据处理过程中，使用了Mapping Tools完成了分析或得到了有价值的帮助，我们期望您在论文发表时，在方法学部分或致谢部分引用或提及Mapping Tools平台。例如：XXXX analysis was performed using the Mapping tools,a free online platform for data analysis <a href="#s">(http://www.omicshare.com/tools</a>)。这样便于更多的同行了解和分享OmicShare平台。
                </p>
              </div>
            </el-card>
          </el-col>
        </el-row>

    </div>
</template>
<script>
import Table from '../Table'
export default {
  components: {
    Table
  },
  data () {
    return {
      loading: false,
      tableData: [
        {
          date: '2016-05-02',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄'
        }, {
          date: '2016-05-04',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1517 弄'
        }, {
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
        }, {
          date: '2016-05-02',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄'
        }, {
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
        }],
      tableColumn: [
        {
          title: '日期',
          key: 'date',
          align: 'center',
          width: 90
        },
        {
          title: '姓名',
          key: 'name',
          align: 'center',
          width: 90
        },
        {
          title: '地址',
          key: 'address',
          align: 'center',
          width: 90
        }
      ]
    }
  },
  methods: {
  },
  created () {
  }
}
</script>
<style lang="less" scope>
.paper {
  margin-top: 15px;
}
.user-button {
  margin-top: 25px;
  // // margin-bottom: 25px;
  // bottom: 0;
  // position: absolute;

}
.user-info {
  .el-col {
    margin-top: 15px;
  }
}
.user-body {
  height: 515px;
  position: relative;
}
</style>
