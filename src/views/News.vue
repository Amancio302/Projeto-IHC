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
  
</style>