<template>
  <div id="check-list" >
    <p style="text-align: center; color: #FFFFFF">
      {{ CheckTitle }}
    </p>
    <check-input @addItem="handleAddItem"></check-input>
    <div v-for="item in CheckList" :key="item.id">
      <check-item :content="item"></check-item>
    </div>
  </div>
</template>

<script>
import CheckItem from '@/components/CheckItem'
import CheckInput from '@/components/CheckInput'
export default {
  name: 'CheckList',
  components: { CheckInput, CheckItem },
  props: {
    CheckTitle: {
      type: String,
      default: "default"
    }
  },
  data() {
    return {
      CheckList: []
    }
  },
  methods: {
    handleAddItem: function (val) {
      this.CheckList.push(val)
    }
  }
}
</script>

<style scoped>
#check-list {
  text-align: left;
  margin-left: 40px;
}
</style>
