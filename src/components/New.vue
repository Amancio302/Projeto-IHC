<template>
  <v-row>
    <v-spacer />
    <v-col cols="auto" v-if="reader">
      <v-btn icon style="background: #f0f0f0" @click="listenTo">
        <v-icon color="#00500f">
          mdi-{{ value !== item.title ? 'volume-high' : 'volume-off'}}
        </v-icon>
      </v-btn>
    </v-col>
    <v-col cols="12">
      <v-card
        flat
        width="100%"
        height="100%"
        :href="item.href"
      >
        <v-row>
          <v-col cols="12">
            <v-img
              height="180"
              contain
              :src="item.image"
            />
          </v-col>
        </v-row>
        <v-row no-gutters>
          <v-col cols="12">
            <div class="new-tag">
              {{ item.tag }}
            </div>
          </v-col>
        </v-row>
        <v-row no-gutters>
          <v-col cols="12">
            <div class="new-title">
              {{ item.title }}
            </div>
          </v-col>
          <v-col cols="auto">
            <v-icon small color="#3c763d">
              mdi-calendar-month-outline
            </v-icon>
          </v-col>
          <v-col cols="3">
            <div class="new-subtitle">
              {{ item.date }}
            </div>
          </v-col>
          <v-col cols="auto">
            <v-icon small color="#337ab7">
              mdi-clock-time-nine-outline
            </v-icon>
          </v-col>
          <v-col cols="3">
            <div class="new-subtitle">
              {{ item.hour }}
            </div>
          </v-col>
        </v-row>
        <v-row no-gutters>
          <v-col cols="12">
            <div class="new-text">
              {{ item.text }}
            </div>
          </v-col>
        </v-row>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'NewComponent',
  props: ['item', 'reader', 'value'],
  methods: {
    async listenTo () {
      if (this.value === this.item.title) {
        this.$emit('input', undefined)
        this.$emit('stop', true)
      } else {
        const msg =
          'Categoria da notícia: ' + this.item.tag +
          '. Postada em: ' + this.item.date + ' ' + this.item.hour +
          '. Título da notícia: ' + this.item.title + 
          '. Descrição da Imagem: ' + this.item.alt +
          '. Resumo da Notícia: ' + this.item.text +
          '. Fim do resumo. Clique na notícia para saber mais.'
        this.$emit('input', this.item.title)
        this.$emit('listen', msg)
      }
    }
  }
}
</script>

<style>
  .new-tag{
    font-family: Arial,Helvetica,sans-serif;
    color: #1759B0;
    text-transform: uppercase;
    font-size: 1.7rem;
    margin-top: .5rem;
    margin-bottom: .5rem;
    padding: 0;
    font-weight: bold;
  }
  .new-title{
    font-family: "open_sanssemibold",'Open Sans',Arial,Helvetica,sans-serif;
    font-size: 2.7rem;
    font-weight: 700;
    color: #333;
  }
  .new-text{
    font-family: "open_sanssemibold",'Open Sans',Arial,Helvetica,sans-serif;
    font-size: 1.7rem;
    color: #444;
  }
</style>