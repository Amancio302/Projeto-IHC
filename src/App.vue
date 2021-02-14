<template>
  <v-app>
    <v-row no-gutters justify="center" class="system-bar ma-0 pa-0">
      <v-spacer/>
      <v-col cols="12" sm="10" md="7">
        <SystemBar />
      </v-col>
      <v-spacer/>
    </v-row>
    <v-row no-gutters class="pa-0 header">
      <v-spacer/>
      <v-col cols="12" sm="10" md="7" class="pa-0 ma-0">
        <Header />
      </v-col>
      <v-spacer />
    </v-row>
    <v-row class="mt-0 pa-0 about">
      <v-col cols="12" class="about ma-0 pa-0">
        <About />
      </v-col>
    </v-row>
    <v-row style="max-height: 50px !important">
      <v-col />
      <v-col cols="7">
        <v-card color="#f0f0f0" flat>
          <v-row align="start">
            <v-col cols="auto">
              <div class="breadcrumbs-text">Você está aqui:</div>
            </v-col>
            <v-col>
              <v-breadcrumbs divider="/" :items="breadcrumbs" class="breadcrumbs" />
            </v-col>
          </v-row>
        </v-card>
      </v-col>
      <v-col />
    </v-row>
    <v-row>
      <v-spacer />
      <v-col cols="7">
        <v-row>
          <v-col cols="3">
            <v-card flat>
              <v-row no-gutters>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-header-btn"
                  >
                    <div class="menu-header-btn-text">
                      Portal UFLA
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Página Principal
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-news-btn menu-news-first"
                  >
                    <div class="menu-news-btn-title">
                      Notícias
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-news-btn"
                  >
                    <div class="menu-news-btn-text">
                      Ensino
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-news-btn"
                  >
                    <div class="menu-news-btn-text">
                      Pesquisa e Inovação
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-news-btn"
                  >
                    <div class="menu-news-btn-text">
                      Extensão e Cultura
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-news-btn"
                  >
                    <div class="menu-news-btn-text">
                      Internacionalização
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-news-btn menu-news-last"
                  >
                    <div class="menu-news-btn-text">
                      Institucional
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Comunicação
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Pró-Reitorias
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Unidades Acadêmicas
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Governaça
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Acesso a sistemas
                    </div>
                  </v-btn>
                </v-col>
              </v-row>
              <v-row no-gutters>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-header-btn"
                  >
                    <div class="menu-header-btn-text">
                      Acesso à Informação
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Institucional
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Ações e Programas
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Participação Social
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Auditorias
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Convênios e Transferências
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Receitas e Despesas
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Licitações e Contratos
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Servidores
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Informações Classificadas
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Serviço de Informação<br>
                      ao Cidadadão - SIC
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Perguntas Frequentes
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Dados Abertos
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Transparência e<br>
                      Prestação de Contas
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Boletim Interno<br>
                      (Atos e Portarias)
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Indicadores
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Projetos com as<br>
                      Fundações de Apoio
                    </div>
                  </v-btn>
                </v-col>
                <v-col cols="12">
                  <v-btn
                    text
                    block
                    class="menu-btn"
                  >
                    <div class="menu-btn-text">
                      Revisão e Consolidação<br>
                      de Atos Normativos
                    </div>
                  </v-btn>
                </v-col>
              </v-row>
            </v-card>
          </v-col>
          <v-col>
            <router-view />
          </v-col>
        </v-row>
      </v-col>
      <v-spacer />
    </v-row>
  </v-app>
</template>

<script>
import SystemBar from '@/components/SystemBar'
import Header from '@/components/Header'
import About from '@/components/About'

export default {
  name: 'App',

  components: {
    SystemBar,
    Header,
    About
  },

  data: () => ({
    breadcrumbs: [
      {
        text: 'Início',
        disabled: false,
        href: 'https://ufla.br',
      },
      {
        text: 'Notícias',
        disabled: false,
        href: 'https://ufla.br/noticias',
      },
    ]
  }),
};
</script>

<style>
  .system-bar{
    background: #ffffff;
    max-height: 33px;
  }
  .header{
    max-height: 150px;
    background-color: #195128 !important;
    background-image: radial-gradient(ellipse at center, #17882c 1%, #00510f 100%) !important;
    color: #fff !important;
    margin: 0;
  }
  * {
      -webkit-box-sizing: border-box;
      -moz-box-sizing: border-box;
      box-sizing: border-box;
  }
  body {
      font-family: "open_sansregular",'Open Sans',Arial,Helvetica,sans-serif;
      color: #333;
      margin: 0;
      background-color: #fff;
  }
  body {
      font-family: "Helvetica Neue",Helvetica,Arial,sans-serif;
      font-size: 14px;
      line-height: 1.42857143;
      color: #333;
      background-color: #fff;
  }
  body {
      font-family: "Helvetica Neue",Helvetica,Arial,sans-serif;
      font-size: 14px;
      line-height: 1.42857143;
      color: #333;
      background-color: #fff;
  }
  html {
      overflow-y: scroll;
      font-size: 100%;
      -ms-text-size-adjust: 100%;
      -webkit-text-size-adjust: 100%;
  }
  html {
      font-size: 10px;
      -webkit-tap-highlight-color: rgba(0,0,0,0);
  }
  html {
      font-family: sans-serif;
      -webkit-text-size-adjust: 100%;
      -ms-text-size-adjust: 100%;
  }
  html {
      font-size: 10px;
      -webkit-tap-highlight-color: rgba(0,0,0,0);
  }
  html {
      font-family: sans-serif;
      -webkit-text-size-adjust: 100%;
      -ms-text-size-adjust: 100%;
  }
  .about{
    background-color: #00420c;
    border-bottom: 2px solid #00420c;
    max-height: 33px;
    padding: 0;
    margin: 0 !important;
  }
  .breadcrumbs{
    align-content: center !important;
    align-items: center !important;
    align-self: center !important;
    max-height: 50px !important;
    margin: 0 !important;
    padding: 0 !important;
  }
  .breadcrumbs-text{
    font-size: 1em !important;
  }
  .menu-header-btn{
    background: -internal-light-dark(rgb(239, 239, 239), rgb(59, 59, 59));
    border: hidden;
    border-top: 3px solid #00500f !important;
    white-space: normal;
    margin-top: 10px;
  }
  .menu-header-btn-text{
    color: #00500f;
    text-transform: uppercase;
    font-size: 1.8em;
    font-family: "open_sanssemibold",'Open Sans',Arial,Helvetica,sans-serif;
    font-weight: 700;
  }
  .menu-btn{
    text-align: start !important;
    text-transform: initial;
    background: #ffffff;
    border: hidden;
    border-bottom: 1px solid #0000 !important;
    white-space: normal;
    max-width: 100%;
    margin-top: 10px;
  }
  .menu-btn-text{
    text-transform: initial;
    font-size: 1.8em;
    font-family: "open_sanssemibold",'Open Sans',Arial,Helvetica,sans-serif;
    font-weight: 500;
    max-width: 100%;
  }
  .menu-news-btn{
    border: hidden;
    background: -internal-light-dark(rgb(239, 239, 239), rgb(59, 59, 59));
    white-space: normal;
    margin-top: 10px;
  }
  .menu-news-first{
    border-top: 2px solid #00500f !important;
  }
  .menu-news-btn-title{
    font-family: "open_sansregular",'Open Sans',Arial,Helvetica,sans-serif;
    font-weight: 700;
    font-size: 1.8em;
    color: #172938;
    text-transform: initial;
  }
  .menu-news-btn-text{
    font-family: "open_sansregular",'Open Sans',Arial,Helvetica,sans-serif;
    font-weight: normal;
    font-size: 1.6em;
    color: #172938;
    text-transform: initial;
  }
  .menu-news-last{
    border-bottom: 3px solid #00500f !important;
    white-space: normal;
    margin-top: 15px;
    padding-top: 10px !important;
    padding-bottom: 10px !important;
  }
</style>
