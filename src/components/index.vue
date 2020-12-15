<template>
  <div class="taskPlan" ref="taskPlanTimeForm" style="width:100%;height:100%">
    <iframe :src="reportUrl" frameborder="0" style="width:100%;" :height="tableHeight" id="iframeBox"></iframe>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      reportUrl: "../../static/html/夜景.html",
      tableHeight:window.screen.availHeight-106.6+'px'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
body {
  margin: 0;
  width: 100%;
  height: 100%;
  background-color: black;
}
</style>
