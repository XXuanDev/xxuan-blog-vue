<!-- 首页 -->
<template>
  <div>
    <sg-navbar></sg-navbar>
    <div class="container">
      <el-row :gutter="30">
        <el-col :sm="24" :md="16" style="transition:all .5s ease-out;margin-bottom:30px;">
          <sg-articlelist></sg-articlelist>
        </el-col>
        <el-col :sm="24" :md="8">
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
import articlelist from '../components/articlelist.vue'
import rightlist from '../components/rightlist.vue'

export default {
  name: 'Home',
  data() { //选项 / 数据
    return {
      recordNumber: '鄂ICP备2024051761号'
    }
  },
  methods: { //事件处理器

  },
  components: { //定义组件
    'sg-navbar': header,
    'sg-articlelist': articlelist,
    'sg-rightlist': rightlist,
  },
  created() { //生命周期函数

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
