<template lang="pug">
  .hello
    .ui.container
      sui-segment(raised='').sunflower
        router-link(to="/course")
          img.logo(src="../assets/logo.png")
        sui-header(size="large") {{ msg }}
        p 學好數學，補習不一定有用！
        p 以個別化的教育方法，量身打造合適的學習進程。
        p 如果在中小學範圍的數學學習上遇到瓶頸，可以先做個數學診斷評估
        p 按
          router-link(to="/course")
            img.ui.mini.inline.image.haha(src="../assets/logo.png")
          | 可以跳到下一頁喔~

</template>

<script>
export default {
  name: 'HelloWorld',
  props: ['likes'],
  data () {
    return {
      msg: '歡迎學習數學，請按圖開始'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
