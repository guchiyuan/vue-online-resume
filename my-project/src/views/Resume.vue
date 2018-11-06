<template>
  <div class="resume">
    <el-container>
      <el-aside class="menu-panel" width="500px">
        <nav>
          <ul>
            <li @click="handlePersonInfoClick()" :class="{active: currentTab === 0}">
              <i class="iconfont" :class="{active: currentTab === 0}">&#xe65d;</i>
              <section>
                <span>About Me</span>
              </section>
            </li>
            <li @click="handleWorkExpClick()" :class="{active: currentTab === 1}">
              <i class="iconfont" :class="{active: currentTab === 1}">&#xe615;</i>
               <section>
                <span>Work Experience</span>
              </section>
            </li>
            <li>
              <i class="iconfont">&#xe609;</i>
              <section>
                <span>Projects</span>
              </section>
            </li>
            <li>
              <i class="iconfont">&#xe8c8;</i>
              <section>
                <span>Education</span>
              </section>
            </li>
            <li>
              <i class="iconfont">&#xe623;</i>
              <section>
                <span>Awards</span>
              </section>
            </li>
            <li>
              <i class="iconfont">&#xe65d;</i>
              <section>
                <span>Contact</span>
              </section>
            </li>
          </ul>
        </nav>
        <section class="person-info editor-panel" v-show="isPersonInfoShow">
          <h1>个人信息</h1>
          <el-form class="form" ref="personInfoform" :model="personInfoform" label-width="80px">
            <el-form-item label="姓名">
              <el-input v-model="personInfoform.name"></el-input>
            </el-form-item>
            <el-form-item label="性别">
              <el-radio-group v-model="personInfoform.sex">
                <el-radio label="糙汉子"></el-radio>
                <el-radio label="萌妹子"></el-radio>
              </el-radio-group>
            </el-form-item>

            <el-form-item label="出生日期">
              <el-col :span="11">
                <el-date-picker type="date" placeholder="选择日期" v-model="personInfoform.birthDate" style="width: 100%;"></el-date-picker>
              </el-col>
            </el-form-item>

             <el-form-item label="姓名">
              <el-input v-model="personInfoform.name"></el-input>
            </el-form-item>
            
          </el-form>
        </section>

        <section class="work-experience editor-panel" v-show="isWorkExpShow">
          <h1>工作经历</h1>

        </section>
      </el-aside>
      <el-main class="content-panel">Main</el-main>
    </el-container>
  </div>
</template> 

<script>


export default {
  name: 'resume',
  data () {
    return {
      currentTab:'',
      isPersonInfoShow: false,
      isWorkExpShow: false,
      personInfoform:{
        name:'',
        sex:'',
        birthDate:''
      }
    }
  },
  components: {
  },
  methods:{
    handlePersonInfoClick () {
      this.currentTab = 0;
      this.isPersonInfoShow = true;
      this.isWorkExpShow = false;
      
    },
    handleWorkExpClick () {
      this.currentTab = 1;
      this.isWorkExpShow = true;
      this.isPersonInfoShow = false;
    }
  }
}
</script>

<style lang="stylus" scoped>
  >>>.iconfont
    font-size 1rem
    color #fff
  nav
    float left
    width 100px
    height 600px
    background-color #0bf
    .active
      background-color #fff
      color #000
    ul
      li
        cursor pointer
        padding 10px
        color #fff
  .menu-panel
    position relative
    margin .3rem
    // background-color #eee
    height 600px
    >>>.el-submenu__title
      background-color #0bf
    .editor-panel
      width 400px
      height 600px
      float left
      .form
        margin-top 50px

  .content-panel
    background-color #666
    margin .3rem
</style>

