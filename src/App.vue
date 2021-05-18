<template>
  <div id="app">
    <el-container>
      <el-header>
        <main-title></main-title>
      </el-header>
      <el-main>
        <el-row>
          <el-col :span="12" class="cus-el-col-l"><div><check-list check-title="✔️"></check-list></div></el-col>
          <el-col :span="12" class="cus-el-col-r"><div><check-list check-title="❌"></check-list></div></el-col>
        </el-row>
      </el-main>
      <el-footer></el-footer>
    </el-container>
  </div>
</template>

<script>
import CheckList from '@/components/CheckList'
import MainTitle from '@/components/MainTitle'

export default {
  name: 'App',
  components: {
    MainTitle,
    CheckList
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#cus-l {
}

#cus-r {
}
.cus-el-col-l {
  background: #42b983;
  padding-bottom: 20px;
}
.cus-el-col-r {
  background: cadetblue;
  padding-bottom: 20px;
}
</style>
