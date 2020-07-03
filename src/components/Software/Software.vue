<template>
  <div class="software">
    <el-card class="box-card">
      <div slot="header" class="clearfix">
        <span>发表论文引用:</span>
      </div>
      <div class="notice">
        <p>
          如果您在数据处理过程中，使用了Mapping Tools完成了分析或得到了有价值的帮助，我们期望您在论文发表时，在方法学部分或致谢部分引用或提及Mapping Tools平台。例如：XXXX analysis was performed using the Mapping tools,a free online platform for data analysis <a href="#s">(http://www.omicshare.com/tools</a>)。这样便于更多的同行了解和分享OmicShare平台。
        </p>
      </div>
    </el-card>
    <div>

      <el-card class="box-card mappings" body-style="{'width':100%,'height':100%}">
        <div class="mappings-header">
          <div class="tab-left">
            <span style="margin-right:20px;font-size:14px;">分类:</span>
            <el-button type="primary" round>所有分类</el-button>
          </div>
          <el-tabs   @tab-click="handleClick" :stretch="true">
            <el-tab-pane label="表格与格式转化" name="1">表格与格式转化</el-tab-pane>
            <el-tab-pane label="动态交互分析" name="2">动态交互分析</el-tab-pane>
            <el-tab-pane label="功能分析" name="3">功能分析</el-tab-pane>
            <el-tab-pane label="基础绘图" name="4">基础绘图</el-tab-pane>
            <el-tab-pane label="聚类分析" name="5">聚类分析</el-tab-pane>
            <el-tab-pane label="统计检验与差异分析" name="6">统计检验与差异分析</el-tab-pane>
            <el-tab-pane label="序列处理" name="7">序列处理</el-tab-pane>
            <el-tab-pane label="注释工具" name="8">注释工具</el-tab-pane>
            <el-tab-pane label="我的收藏" name="9">我的收藏</el-tab-pane>
          </el-tabs>
        </div>
        <div class="meppings-middle">
          <el-input placeholder="请输入内容" clearable style="width:200px">
            <i slot="suffix" class="el-input__icon el-icon-search"></i>
          </el-input>
          <el-switch active-text="最新" inactive-text="最热"></el-switch>
        </div>

        <div class="meppings-bootm">
          <el-row :gutter="10">
            <el-col :xs="24" :sm="24" :md="12"  :lg="8" :xl="6" ><!-- -->
              <div class="grid-content" >
                <el-card class="maps-card" body-style="{ padding: '15px';margin:'10px'; position: 'relative';}">
                  <div  class="maps-image">
                    <img src="../../assets/software_map/reportheatmap.png">
                  </div>
                  <div class="maps-content">
                    <span>动态热图</span>
                    <div class="bottom clearfix">
                      <!-- <time class="time">{{ currentDate }}</time> -->
                      <div style="font-family:Arial;">
                        将表格数据绘制成一个热图
                      </div>

                    </div>
                  </div>
                </el-card>
              </div>
            </el-col>
            <el-col  :xs="24" :sm="24" :md="12"  :lg="8" :xl="6"><!-- -->
              <div class="grid-content" >
                <el-card class="maps-card" body-style="{ padding: '15px';margin:'10px'; position: 'relative';}">
                  <div  class="maps-image">
                    <img src="../../assets/software_map/reportheatmap.png">
                  </div>
                  <div class="maps-content">
                    <span>动态热图</span>
                    <div class="bottom clearfix">
                      <!-- <time class="time">{{ currentDate }}</time> -->
                      <div style="font-family:Arial;">
                        将表格数据绘制成一个热图
                      </div>

                    </div>
                  </div>
                </el-card>
              </div>
            </el-col>
            <el-col :xs="24" :sm="24" :md="12"  :lg="8" :xl="6" ><!-- -->
              <div class="grid-content" >
                <el-card class="maps-card" body-style="{ padding: '15px';margin:'10px'; position: 'relative';}">
                  <div  class="maps-image">
                    <img src="../../assets/software_map/reportheatmap.png">
                  </div>
                  <div class="maps-content">
                    <span>动态热图</span>
                    <div class="bottom clearfix">
                      <!-- <time class="time">{{ currentDate }}</time> -->
                      <div style="font-family:Arial;">
                        将表格数据绘制成一个热图
                      </div>

                    </div>
                  </div>
                </el-card>
              </div>
            </el-col>
            <el-col  :xs="24" :sm="24" :md="12"  :lg="8" :xl="6"><!-- -->
              <div class="grid-content" >
                <el-card class="maps-card" body-style="{ padding: '15px';margin:'10px'; position: 'relative';}">
                  <div  class="maps-image">
                    <img src="../../assets/software_map/reportheatmap.png">
                  </div>
                  <div class="maps-content">
                    <span>动态热图</span>
                    <div class="bottom clearfix">
                      <!-- <time class="time">{{ currentDate }}</time> -->
                      <div style="font-family:Arial;">
                        将表格数据绘制成一个热图
                      </div>

                    </div>
                  </div>
                </el-card>
              </div>
            </el-col>
            <el-col :xs="24" :sm="24" :md="12"  :lg="8" :xl="6" ><!-- -->
              <div class="grid-content" >
                <el-card class="maps-card" body-style="{ padding: '15px';margin:'10px'; position: 'relative';}">
                  <div  class="maps-image">
                    <img src="../../assets/software_map/reportheatmap.png">
                  </div>
                  <div class="maps-content">
                    <span>动态热图</span>
                    <div class="bottom clearfix">
                      <!-- <time class="time">{{ currentDate }}</time> -->
                      <div style="font-family:Arial;">
                        将表格数据绘制成一个热图
                      </div>

                    </div>
                  </div>
                </el-card>
              </div>
            </el-col>
            <el-col  :xs="24" :sm="24" :md="12"  :lg="8" :xl="6"><!-- -->
              <div class="grid-content" >
                <el-card class="maps-card" body-style="{ padding: '15px';margin:'10px'; position: 'relative';}">
                  <div  class="maps-image">
                    <img src="../../assets/software_map/reportheatmap.png">
                  </div>
                  <div class="maps-content">
                    <span>动态热图</span>
                    <div class="bottom clearfix">
                      <!-- <time class="time">{{ currentDate }}</time> -->
                      <div style="font-family:Arial;">
                        将表格数据绘制成一个热图
                      </div>

                    </div>
                  </div>
                </el-card>
              </div>
            </el-col>
          </el-row>

        </div>
      </el-card>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {

    }
  },
  methods: {
    handleClick () {}
  }
}
</script>
<style lang="less" scope>
.clearfix span{
  font-weight: bold;
}
.notice p{
  line-height:30px;
  font-size: 14px;
  text-align: justify;
}
.mappings {
  position: relative;
  margin-top: 20px;
}
.tab-left{
  float:left;
  position:relative;
  margin-top:5px;
  margin-right: 25px;
}
.meppings-heared{
  margin-top: 10px;
  width: 100%;
  position: relative;
}
.meppings-middle{
  // position: relative;
  // float: right;
  margin-right: 50px;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  margin-bottom: 10px;
}
.maps-image{
  padding: 20px;
  float: left;
}
.maps-content{
  float: right;
  width: 220px;
}
.maps-card{
  // margin-top: 70px;
}
.grid-content{
  padding-top:15px;
  width: 396px;
}
row{
  // display: flex;
  // flex-wrap:wrap;
}
</style>
