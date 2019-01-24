<template>
  <div class="homeWrap">
    <el-menu :default-active="activeIndex"
        class="el-menu-demo" mode="horizontal" background-color="#091e9e"
        text-color="#fff" active-text-color="#ffd04b">
        <el-menu-item index="1" style="pointer-events: none">
            <img src="../assets/logo.png" height="62" width="385">
        </el-menu-item>
        <el-menu-item index="2" style="margin-left: 10%">首页</el-menu-item>
        <el-menu-item index="3">关于我们</el-menu-item>
        <el-menu-item index="4">服务项目</el-menu-item>
        <el-menu-item index="5">行业动态</el-menu-item>
        <el-menu-item index="6">联系我们</el-menu-item>
    </el-menu>
    <div class="homeBan">
       <img src="../assets/backg.png" height="300" width="100%">
    </div>
    <div class="homeCon">
        <div class="homeContent">
            <h2 style="line-height: 45px;">企业愿景</h2>
            <hr>
            <div class="contentWrap" v-for="cons in conData">
                <h3>{{cons.title}}</h3>
                <p>{{cons.content}}</p>
              <div class="contImg">
                <img :src="cons.imgUrl" height="210" width="773" />
              </div>  
            </div>
        </div>

    </div>
    <div class="footer">
      <div>
            版权所有：陕西科大高新教育科技投资有限公司 电话：029-81552035<br>
             西安市长安区子午大道中段39号　邮编：710109
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
     activeIndex: '2',
     conData:[{
        title: '助力教育发展',
        content: '教育，通过以学生主动探索为中心的课程活动设计、引入业界广泛应用的软硬件平台、以及参与工程挑战竞赛活动，激发孩子们对科技的兴趣，帮助他们广泛地接触科技知识，掌握常用工程工具的使用方法，训练工程思维，培养其勇于接受工程挑战、主动学习、以及综合运用知识解决问题的能力...',
        imgUrl: require('../assets/cont.png')
     },{
        title: '助力软件研发',
        content: '教育移动APP的内容量巨大，且繁杂。尤其是针对学生使用的APP，既有数学公式、化学图形、语文古文、还有外语习题，而且还要分年级和不同的教学内容。学生端需要提交作业，教师端需要打分数，因此一款教育APP软件开发日常的更新成为了开发的难点，不仅量大，而且更新界面布局也不同...',
        imgUrl: require('../assets/con_c.png')
      },{
        title: '助力基础建设',
        content: '为社会生产和居民生活提供公共服务的物质工程设施，它是社会赖以生存发展的一般物质条件。基础设施不仅包括公路、水电煤气等公共设施，即俗称的基础建设，亦都包括教育社会事业即基础设施...',
        imgUrl: require('../assets/con_b.png')
      }]
    }
  },
  mounted(){
    
  }
}
</script>
<style>
.homeWrap{
  background-color: #f9f8f8;
}
.el-menu--horizontal>.el-menu-item{
  height: 65px;
  line-height: 65px;
}
.el-menu-demo{
  padding-left: 10%;
}
.el-menu-item{
  font-size: 16px;
}
.homeBan{
  width: 100%;
}
.homeCon{
  width: 100%;
  height: 1200px;
  position: relative;
}
.homeContent{
  width: 74%;
  height: auto;
  background-color: white;
  box-shadow:0px 0px 20px rgba(218,215,215,0.9);
  position: absolute;
  left: 13%;
  top: -50px;
}
.contentWrap{
  width: 80%;
  margin: 0 auto;
}
.contImg{
  margin-top: 20px;
  margin-bottom: 20px;
  overflow: hidden;
}
.contImg img{
  transition: all 1s;
}
.contImg img:hover{
  -webkit-transform: scale(1.1);
     -moz-transform: scale(1.1);
      -ms-transform: scale(1.1);
       -o-transform: scale(1.1);
          transform: scale(1.1);
}
.contentWrap p,.contentWrap h3{
  margin-top: 20px;
}
.contentWrap p{
  text-indent: 2em;
}
.footer{
  width: 100%;
  height: 100px;
  background-color: #5f5a59;
}
.footer div{
  padding-top: 25px;
  color: #999;
}
</style>
