<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>狩りに必要なアイテムを買おう！</h2>
    <h2>このアイテムはユーザーと売買できるぞ！</h2>
    <h2>剣や盾や回復薬などのアイテムが選べます。</h2>
    <img src="../assets/kaihuku.png">
    <img src="../assets/tate.jpg">
    <img src="../assets/ken.jpg">

    <el-row>
      <el-col :span="8" v-for="(o, index) in 2" :key="o" :offset="index > 0 ? 2 : 0">
        <el-card :body-style="{ padding: '0px' }">
          <img src="../assets/kaihuku.png" class="image">
          <div style="padding: 14px;">
            <span>回復薬</span>
            <div class="bottom clearfix">
              <el-button type="text" class="button">Buy</el-button>
            </div>
          </div>
        </el-card>
      </el-col>
    </el-row>

    <div class="float-panel">
    <el-card :body-style="{ padding: '10px 15px' }">
      <img src="../assets/kaihuku.png">

    </el-card>

    </div>

  </div>


</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'クリプトハンターズ 狩りしようぜ'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>


<style>
  .time {
    font-size: 13px;
    color: #999;
  }
  
  .bottom {
    margin-top: 13px;
    line-height: 12px;
  }

  .button {
    padding: 0;
    float: right;
  }

  .image {
    width: 100%;
    display: block;
  }

  .clearfix:before,
  .clearfix:after {
      display: table;
      content: "";
  }
  
  .clearfix:after {
      clear: both
  }
</style>

<script>
export default {
  data() {
    return {
      currentDate: new Date()
    };
  }
}
</script>


<style>
    .float-panel{
        right: 50px;
        top: 50px;
        border-radius: 10px;
    }
</style>