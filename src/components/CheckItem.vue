<template>
  <div>
    <el-row>
      <el-col :span="24">
        <el-checkbox v-model="checked" @change="setColor">
          <span :style="{color: checked_color}">{{content}}</span>
          </el-checkbox>
      </el-col>
    </el-row>
  </div>

</template>

<script>
export default {
  name: 'check-item',
  props: {
    content: String
  },
  data () {
    return {
      checked: false,
      checked_color: "#FFFFFF"
    }
  },
  methods: {
    setColor: function () {
      if (this.checked === true) {
        this.checked_color="#000000"
      }else {
        this.checked_color="#FFFFFF"
      }
    }
  }
}
</script>

<style scoped>
.el-checkbox{
  margin: 5px;
}
</style>
