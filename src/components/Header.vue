<template>
  <v-container class="ma-0 pa-0">
    <v-row no-gutters class="pb-0 mb-0">
      <v-col cols="auto">
        <v-btn
          class="header-navigation-btn"
          block
          text
          height="13"
          to="#content"
          @click="scrollToElement('content')"
        >
          <div class="header-navigation-text">Ir para o conteúdo</div> <div class="header-navigation-number"> 1</div>
        </v-btn>
      </v-col>
      <v-col cols="auto">
        <v-btn
          class="header-navigation-btn"
          block
          text
          height="13"
        >
          <div class="header-navigation-text">Ir para o menu</div> <div class="header-navigation-number"> 2</div>
        </v-btn>
      </v-col>
      <v-col cols="auto">
        <v-btn
          class="header-navigation-btn"
          block
          text
          height="13"
          to="#search"
          @click="scrollToElement('search')"
        >
          <div class="header-navigation-text">Ir para a busca</div> <div class="header-navigation-number"> 3</div>
        </v-btn>
      </v-col>
      <v-col cols="auto">
        <v-btn
          class="header-navigation-btn"
          block
          text
          height="13"
        >
          <div class="header-navigation-text">Ir para o rodapé</div> <div class="header-navigation-number"> 4</div>
        </v-btn>
      </v-col>
      <v-spacer />
      <v-col cols="auto">
        <v-btn
          class="header-acessibility-btn"
          block
          text
          height="13"
          href="https://ufla.br/acessibilidade"
        >
          <div class="header-acessibility-text">Acessibilidade</div>
        </v-btn>
      </v-col>
      <v-col cols="auto">
        <v-btn
          class="header-acessibility-btn"
          block
          text
          height="13"
        >
          <div class="header-acessibility-text">Alto Contranste</div>
        </v-btn>
      </v-col>
      <v-col cols="auto">
        <v-btn
          class="header-acessibility-btn"
          block
          text
          height="13"
          href="https://ufla.br/sitemap"
        >
          <div class="header-acessibility-text">Sitemap</div>
        </v-btn>
      </v-col>
    </v-row>
    <v-row dense align="center" align-content="center">
      <v-col cols="auto">
        <v-img
          src="https://ufla.br/templates/portalufla/images/ufla-logo.png"
          alt="Logomarca da Ufla, circulo azul com duas linhas paralelas até o centro e do centro para baixo"
          class="logo-ufla"
          height="80px"
        />
      </v-col>
      <v-col>
        <v-row no-gutters>
          <v-col cols="12" style="max-height: 1px">
            <div class="header-text">Ministério da Educação</div>
          </v-col>
          <v-col cols="12" style="max-height: 60px">
            <div class="header-title">Portal UFLA</div>
          </v-col>
          <v-col cols="12" style="max-height: 1px">
            <div class="header-subtitle">Universidade Federal de Lavras</div>
          </v-col>
        </v-row>
      </v-col>
      <v-spacer />
      <v-col cols="3">
        <v-row no-gutters>
          <v-col cols="12" tag="search">
            <v-text-field
              label="Busca Portal UFLA"
              autofocus
              single-line
              type="text"
              append-icon="mdi-magnify"
              background-color="#ffffff"
            />
          </v-col>
          <v-col cols="auto">
            <v-btn icon href="http://pt-br.facebook.com/uflabr/">
              <v-icon color="#fafafa">
                mdi-facebook
              </v-icon>
            </v-btn>
          </v-col>
          <v-col cols="auto">
            <v-btn icon href="https://twitter.com/uflabr">
              <v-icon color="#fafafa">
                mdi-twitter
              </v-icon>
            </v-btn>
          </v-col>
          <v-col cols="auto">
            <v-btn icon href="https://www.instagram.com/uflabr/">
              <v-icon color="#fafafa">
                mdi-instagram
              </v-icon>
            </v-btn>
          </v-col>
          <v-col cols="auto">
            <v-btn icon href="https://api.whatsapp.com/send?phone=5535992720134&text=Ol%C3%A1,%20quero%20me%20inscrever%20para%20receber%20mensagens%20da%20UFLA">
              <v-icon color="#fafafa">
                mdi-whatsapp
              </v-icon>
            </v-btn>
          </v-col>
          <v-col cols="auto">
            <v-btn icon href="https://ufla.br/noticias/institucional/13560-lancado-canal-informativo-pelo-telegram-confira-como-aderir">
              <v-icon color="#fafafa">
                mdi-telegram
              </v-icon>
            </v-btn>
          </v-col>
          <v-col cols="auto">
            <v-btn icon href="https://www.youtube.com/user/uflabr">
              <v-icon color="#fafafa">
                mdi-youtube
              </v-icon>
            </v-btn>
          </v-col>
          <v-col cols="auto">
            <v-btn icon href="https://www.linkedin.com/school/uflabr/">
              <v-icon color="#fafafa">
                mdi-linkedin
              </v-icon>
            </v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Header',
  methods: {
    scrollToElement (el) {
      const aux = this.$el.getElementsByTagName(el)[0]
      aux.scrollIntoView({behavior: 'smooth'});
    }
  }
}
</script>

<style>
  .header-navigation-btn{
    border: hidden;
    background: transparent !important;
  }
  .header-navigation-btn:hover{
    background-color: #cad2cc !important;
  }
  .header-navigation-text{
    color: #dcffe3;
    font-size: 1em;
    background-color: transparent;
    text-transform: initial;
    line-height: 10px;
    font-family: Arial,Helvetica,sans-serif !important;
    margin: 0;
    line-height: 5px;
    padding-top: 2px;
  }
  .header-navigation-number{
    background-color: #cad2cc;
    color: #195128;
    padding: 0 2px 0 3px;
    font-family: Arial,Helvetica,sans-serif !important;
    margin: 0;
    padding-top: 2px;
  }
  .header-acessibility-btn{
    border: hidden;
    background: transparent !important;
  }
  .header-acessibility-btn:hover{
    border-bottom: thin;
  }
  .header-acessibility-text{
    text-transform: uppercase;
    color: white;
    font-family: "open_sansregular",'Open Sans',Arial,Helvetica,sans-serif;
  }
  .header-text{
    font-size: .85em;
    height: 20px;
    color: #ffffff;
    font-family: "open_sansregular",'Open Sans',Arial,Helvetica,sans-serif;
    line-height: 1.42857143;
  }
  .header-title{
    font-family: "open_sansextrabold",'Open Sans',Arial,Helvetica,sans-serif;
    font-size: 2.75em;
    line-height: .8em;
    font-weight: 800;
    letter-spacing: -1px;
    margin-bottom: 3px;
    margin-block-start: 0.67em;
    margin-block-end: 0.67em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    color: #ffffff;
  }
  .header-subtitle{
    font-size: 1.1em;
    text-transform: uppercase;
    position: relative;
    top: 4px;
    font-family: "open_sansregular",'Open Sans',Arial,Helvetica,sans-serif;
    color: #ffffff;
  }
  .logo-ufla{
    max-height: 80px;
  }
</style>