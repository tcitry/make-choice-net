<template>
<div>
  <el-row :gutter="20">
    <el-col :span="20">
      <el-input type="text" v-model="InputValue" @keypress.enter.native="addItem(InputValue)"></el-input>
    </el-col>
    <el-col :span="4">
      <el-button @click="addItem(InputValue)">确认</el-button>
    </el-col>
  </el-row>
</div>
</template>

<script>

let InputValue = ""
export default {
  name: 'CheckInput',
  props: {
  },
  data:function() {
    return{
      InputValue: InputValue
    }
  },
  methods: {
    addItem: function (val) {
      if (val !== "") {
        this.$emit('addItem', val)
        this.InputValue = ""
      }
    }
  }
}
</script>

<style scoped>
.el-col {
  margin-bottom: 20px;
}
</style>
