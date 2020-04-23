<template lang="pug">
  .hello.ui.container
    sui-header(size="large") {{ msg }}
    router-link(to="/chat")
      img.logo(src="../assets/logo.png")
    sui-segment(raised='', padded='', align='left')
      sui-header(size="large") 其他問題？
      p.ans
        a(href="mailto:bestian@gmail.com", target="_blank")
          | 洽詢: bestian@gmail.com

</template>
<script>
export default {
  name: 'FAQ',
  props: ['likes'],
  data () {
    return {
      msg: '常見問題'
    }
  },
  methods: {
    scrollFix: function (hashbang) {
      window.scroll({
        top: hashbang,
        behavior: 'smooth'
      })
    }
  },
  mounted: function () {
    setTimeout(() => this.scrollFix(this.$route.params.bookmark), 100)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.tada {
  position: relative;
  animation: tada 4s infinite;
}

@keyframes tada {
  0%   {color:red; left:-5vw; top:0px;}
  50%  {color:blue; left:5vw; top:0x;}
  100% {color:red; left:-5vw; top:0px;}
}

</style>
