<!-- 文章详情 -->
<template>
    <div>
        <sg-nav></sg-nav>
        <div  class="container" id="detail">
            <el-row  :gutter="30">
                <el-col :sm="24" :md="16" style="transition:all .5s ease-out;margin-bottom:30px;">
                    <sg-articleDetail></sg-articleDetail>
<!--                    <sg-message></sg-message>-->
                </el-col>
                <el-col :sm="24"  :md="8" >
                    <sg-rightlist></sg-rightlist>
                </el-col>
            </el-row>
        </div>
      <footer id="foot">
        <p>©2024 Created by XXuan</p>
        <p><a id="miit" href="https://beian.miit.gov.cn" target="_blank">{{ recordNumber }}</a></p>
      </footer>
    </div>

</template>

<script>
import header from '../components/header.vue'
import rightlist from '../components/rightlist.vue'
import articleDetail from '../components/articleDetail.vue'
import message from '../components/message.vue'
    export default {
        name:'DetailShare',
        data() { //选项 / 数据
            return {
              recordNumber: '鄂ICP备2024051761号',
            }
        },
        methods: { //事件处理器

        },
        components: { //定义组件
            'sg-nav':header,
            'sg-articleDetail':articleDetail,
            'sg-message':message,
            'sg-rightlist':rightlist,
        },
        created() { //生命周期函数

        },
        mounted(){
            var anchor = document.querySelector("#detail");
            // console.log(anchor,anchor.offsetTop);
            var top = anchor.offsetTop-60;
            document.body.scrollTop = top;
             // Firefox
             document.documentElement.scrollTop = top;
             // Safari
             window.pageYOffset = top;
        }
    }
</script>

<style>
#foot {
  /*background-color: #007bff;*/
  background-color: #007bff;
  color: #fff;
  padding: 10px 0;
  text-align: center;
}

#miit {
  color: #fff;
}

</style>
