<template lang="pug">
  .hello
    .ui.container
      sui-segment(raised='').heart
        sui-header(size="large") {{ msg }}
        router-link(to="/faq")
          img.logo(src="../assets/logo.png")
        sui-header(size="large") 要怎麼付費呢?
          .ui.sub.header 診斷面交，遠距課診轉帳~
        br
        br
        sui-grid(:columns="2" divided)
          sui-grid-row
            sui-grid-column
              sui-header(size="medium") 學習診斷
                .ui.sub.header
                  | 隨喜
            sui-grid-column
              sui-header(size="medium") Haskell學習
                .ui.sub.header
                  | $NT1000 / 次
</template>
<script>
export default {
  name: 'Payment',
  data () {
    return {
      msg: '收費標準'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.tada {
  position: relative;
  animation: tada 4s infinite;
}

</style>
