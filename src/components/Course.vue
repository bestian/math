<template lang="pug">
  .hello
    .ui.container
      sui-segment(raised='').code
        sui-header(size="large") {{ msg }}
        router-link(to="/flow")
          img.logo(src="../assets/logo.png")
        sui-header(size="large") 數學有困難嗎?
          .sub.header 和Bestian一起找到事半功倍的學習方法吧
        br
        br
        sui-grid(:columns="3" doubling divided)
          sui-grid-row
            sui-grid-column
              sui-header(size="medium") 學習診斷是什麼
              sui-list(ordered)
                a(is="sui-list-item" v-for="q in qs", :key="q.n", :href="q.h", target="_blank")
                  img(:src="'https://www.google.com/s2/favicons?domain=' + q.h")
                  | {{ q.n }}

            sui-grid-column
              sui-header(size="medium") Bestian的作品
              sui-list(ordered)
                a(is="sui-list-item" v-for="w in works", :key="w.n", :href="w.h", target="_blank")
                  img(:src="'https://www.google.com/s2/favicons?domain=' + w.h")
                  | {{ w.n }}
            sui-grid-column
              sui-header(size="medium") Bestian是誰
              sui-list(ordered)
                a(is="sui-list-item" v-for="b in bestians", :key="b.n", :href="b.h", target="_blank")
                  img(:src="'https://www.google.com/s2/favicons?domain=' + b.h")
                  | {{ b.n }}
</template>

<script>
export default {
  name: 'Course',
  data () {
    return {
      msg: '學習診斷',
      qs: [
        {n: '數學學習診斷是什麼?', h: 'https://docs.google.com/document/d/14KB9cukNH3pF3ZYNGG79w8WMD77EYb7dxGEQ7vzxeGc/edit?usp=sharing'},
        {n: '倒溯法', h: 'https://docs.google.com/document/d/1ydDzS_FjrP1hUqrsHxHsvB-1cG4pi9Rcxx-OgGNOUII/edit?usp=sharing'}
      ],
      works: [
        {n: '零時黑板', h: 'http://goban.tw'},
        {n: '自由數學', h: 'http://math.alearn.org.tw'},
        {n: '自學地圖', h: 'http://map.alearn.org.tw'},
        {n: '自學2.0', h: 'http://we.alearn.org.tw'},
        {n: '認照片遊戲', h: 'http://elder.game.tw'},
        {n: '走失聯絡卡', h: 'http://imlost.bestian.tw'},
        {n: '小巴開發的手機App', h: 'http://goban.tw/#/see/bestian_apps/0/0'},
        {n: '更多小巴開發的網站', h: 'http://goban.tw/#/see/bestian_apps/0/0'}
      ],
      bestians: [
        {n: 'Bestian@github', h: 'https://www.github.com/bestian'},
        {n: 'Bestian@Facebook', h: 'https://www.facebook.com/bestiant'},
        {n: 'Bestian@LinkedIn', h: 'https://www.linkedin.com/in/bestian-tang-5a968843/'}
      ]
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

@keyframes tada {
  0%   {color:red; left:-5vw; top:0px;}
  50%  {color:blue; left:5vw; top:0x;}
  100% {color:red; left:-5vw; top:0px;}
}

</style>
