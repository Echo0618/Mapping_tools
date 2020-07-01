<template>
    <el-container class="home-container">
        <!-- 头部区域 -->
        <el-header>
            <div>
                <!-- <img src="../assets/logo.png" alt=""> -->
                <span>北京胜时代生物科技有限公司--绘图工具</span>
            </div>
            <el-button type="info" @click="logout">退出</el-button></el-header>
        <!-- 主题区域 -->
        <el-container>
            <!-- 侧边栏  -->
            <el-aside width="160px">
                <el-menu :unique-opened="true" :collapse="isCollapse" :collapse-transition="false" :router="true" :default-active="activePath" background-color="#2680AF" text-color="#fff" active-text-color="#409eff">
                    <el-menu-item :index="'/'+subItem.path" @click="saveNavState('/'+subItem.path)" v-for="subItem in menuList" :key="subItem.id">
                            <template slot="title">
                                <!-- 图标 -->
                                <i :class="iconsObj[subItem.id]"></i>
                                <!-- 文本 -->
                                <span>{{subItem.authName}}</span>
                            </template>
                        </el-menu-item>
                    </el-menu>
            </el-aside>
            <!-- 右侧内容主题 -->
            <el-main>
                <router-view></router-view>
            </el-main>
        </el-container>
    </el-container>
</template>

<script>
export default {
  components: {
  },
  data () {
    return {
      menuList: [
        {
          path: 'users',
          id: 'user',
          authName: '个人中心'
        }, {
          path: 'software',
          id: 101,
          authName: '软件中心'
        }],
      iconsObj: {
        user: 'iconfont icon-user',
        103: 'iconfont icon-tijikongjian',
        101: 'iconfont icon-shangpin',
        102: 'iconfont icon-danju',
        145: 'iconfont icon-baobiao'
      },
      isCollapse: false,
      activePath: ''
    }
  },
  methods: {
    logout () {
      window.sessionStorage.clear()
      this.$router.push('/login')
    },
    // async getMenuList () {
    //   const { data: res } = await this.$http.get('menus')
    //   if (res.meta.status !== 200) return this.$message.error(res.meta.msg)
    //   this.menuList = res.data
    // },
    toggleCollapse () {
      this.isCollapse = !this.isCollapse
    },
    saveNavState (activePath) {
      window.sessionStorage.setItem('activePath', activePath)
      this.activePath = activePath
    }
  },
  created () {
    // this.getMenuList()
    this.activePath = window.sessionStorage.getItem('activePath')
  }
}
</script>
<style lang="less" scope="">
.home-container{
    height: 100%;
}
.el-header{
    background-color: #14577A;
    display: flex;
    justify-content: space-between;
    padding-left: 0;
    align-items: center;
    color: #fff;
    font-size: 20px;
    > div {
        display: flex;
        align-items: center;
        span {
            margin-left: 15px;
        }
    }
}
.el-aside{
    background-color: #2680AF;
    .el-menu{
        border-right: none;
    }
}
.el-main{
    background-color: #eaedf1;
}
.iconfont{
    margin-right: 10px;
}
.toggle-button{
    background-color: #4A5064;
    color: #fff;
    text-align:center;
    font-size: 10px;
    line-height: 24px;//行高
    letter-spacing: 0.2em;// 字间距
    cursor: pointer;// 鼠标放上去变小手
}
</style>
