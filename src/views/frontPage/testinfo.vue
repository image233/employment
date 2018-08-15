<template>
<div>
    ????????
  <div>
    <el-tabs v-model="activeName" @tab-click="handleClick">
    <el-tab-pane label="tab1" name="first">tab1</el-tab-pane>
    <el-tab-pane label="tab2" name="second">tab2</el-tab-pane>
    <el-tab-pane label="tab3" name="third">tab3</el-tab-pane>
    <el-tab-pane label="tab4" name="fourth">tab4</el-tab-pane>
  </el-tabs>
  </div>
  </div>
</template>

<script>
export default {
    data() {
      return {
        activeName: 'second'
      };
    },
    methods: {
      handleClick(tab, event) {
        console.log(tab, event);
      }
    }
};
</script>

<style scoped>

</style>
