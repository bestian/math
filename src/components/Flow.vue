<template lang="pug">
  .hello
    .ui.container
      sui-segment(raised='').ranged
        sui-header(size="large") {{ msg }}
        router-link(to="/payment")
          img.logo(src="../assets/logo.png")
        p 透過焦點解決的方法，達到以下目標：

      sui-grid(:columns="3", divided)
        sui-grid-row
        sui-grid-row
          sui-grid-column
          sui-grid-column
            sui-list(bulleted='' align="left")
              sui-list-item 移除不良的學習方法和學習習慣
              sui-list-item 找到「事半功倍」的自學方法
              sui-list-item 提高學習效率
              sui-list-item 重建對數學的成就感和信心
          sui-grid-column
        sui-grid-row
          sui-grid-column
          sui-grid-column
            a(href="https://docs.google.com/forms/d/e/1FAIpQLSeG2FvsquNvKMC9E6lsGRiePDZd3NI6P6SLnkogmRWp-NHdDg/viewform", target="_blank") 預約手術請填此表
          sui-grid-column
        sui-grid-row
</template>

<script>
export default {
  name: 'Flow',
  data () {
    return {
      msg: '學習手術'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
