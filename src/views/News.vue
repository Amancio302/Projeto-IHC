<template>
  <v-container class="pa-0 ma-0" tag="content">
    <v-row>
      <v-col>
        <div class="news-title">
          Notícias
        </div>
      </v-col>
      <v-spacer/>
      <v-col cols="auto">
        <v-btn
          block
          text
          style="border: hidden;
          background: transparent !important;"
          to="news"
        >
          <div class="news-title">Ativar leitor de notícias</div>
        </v-btn>
      </v-col>
    </v-row>
    <v-row>
      <v-col
        cols="4"
        v-for="(noticia, i) in noticias"
        :key="i"
      >
        <New
          :item="noticia"
          class="new-container"
        />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import New from '@/components/New'
import myNews from '@/assets/info/news'

export default {
  name: 'News',
  components: {
    New
  },
  data: () => ({
    noticias: [],
    listener: new SpeechSynthesisUtterance(),
  }),
  created () {
    console.log(myNews)
    this.noticias = myNews.map(el => {
      console.log(el)
      return {
        ...el,
        playing: false
      }
    })
    console.log(this.noticias)
  },
  watch: {
    isPlaying: function (val) {
      alert(val)
    }
  },
  methods: {
    onListen (msg, i) {
      if (!window.speechSynthesis.speaking) {
        this.play(msg, i)
      } else {
        this.stop(i)
      }
    },
    async play (msg, i) {
      console.log('play')
      this.noticias[i].playing = true
      this.listener.text = msg
      window.speechSynthesis.speak(this.listener)
      await new Promise((resolve) => {
        this.listener.onend = resolve
        this.noticias[i].playing = false
      })
    },
    stop (i) {
      console.log('stop')
      this.noticias[i].playing = false
      window.speechSynthesis.cancel()
    }
  }
}
</script>

<style>
  .news-title{
    color: #00500f;
    font-size: 2em;
    font-weight: 700;
    border: 0;
  }
  .new-container{
    margin-bottom: 30px !important;
  }
</style>