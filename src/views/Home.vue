<template>

  <div>
      <div class="divPopover">
<!--        <el-popover-->
<!--            class="popover"-->
<!--            placement="top-start"-->
<!--            title="标题"-->
<!--            width="200"-->
<!--            trigger="hover"-->
<!--            content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。">-->
<!--          <img slot="reference" class="imgAvatar" src="https://himg.bdimg.com/sys/portrait/item/public.1.b7becd36.DkcqTatgpAI4Ggt97ruc9Q.jpg">-->
<!--        </el-popover>-->
<!--        <span style="margin-top: 14px">-->
<!--          123-->
<!--        </span>-->
      </div>
    <div  style="margin-top: 12%">
      <img src="../assets/logo.png" style="width: 240px" @click="doOpenBlog">
    </div>
    <div style="margin-top:10px">
      <el-input v-model="searchInput" @keydown.enter.native="doSearch" placeholder="请输入搜索内容..."></el-input>
      <el-button type="primary" @click="doSearch">百度一下</el-button>
    </div>
  </div>
</template>

<script>
export default {
name: "home",
  data(){
    return{
      abc:true,
      searchInput:''
    }
  },
  mounted() {
    console.log("%c欢迎使用纯净版 Baidu，我们只为追求极简。\nGithub:https://github.com/Jimecc","color:pink");
  },
  methods:{
    change(){
      this.abc = !this.abc;
    },
    doSearch(){
      if(this.searchInput != null && this.searchInput != ''){
        window.open('https://www.baidu.com/s?wd='+this.searchInput,'_self');
      }
    },
    doOpenBlog(){
      window.open('http://jime.cc/','_self');
    }
  }
}
</script>

<style scoped>
.divClass{
  display: flex;
}
.el-input{
  width:40%;
  border-radius: 10px 0 0 10px;

}

.el-button {
  background: #4e6ef2;
  border-radius: 0 12px 12px 0;
}


.imgAvatar{
  width: 30px;
  border: 2px solid #4e6ef2;
  box-sizing: content-box;
  border-radius: 30px;
  /*filter: blur(5px);*/
}

.divPopover{
  text-align: right;
  margin-right: 60px;
}
</style>
