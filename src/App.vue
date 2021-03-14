<template>
  <v-app>
    <v-row no-gutters justify="center" align="start">
      <v-col cols="12" sm="10" md="7">
        <v-row no-gutters style="overflow-x: auto">
          <v-col xl="auto">
            <v-btn
              class="barra-brasil-btn"
              block
              text
              outlined
              @click="reader = !reader"
            >
              <div class="barra-brasil-text">{{ reader ? 'Desativar' : 'Ativar' }} leitor de notícias</div>
            </v-btn>
          </v-col>
          <v-col xl="auto">
            <v-btn
              class="barra-brasil-btn"
              block
              text
              outlined
              href="https://gov.br"
            >
              <div class="barra-brasil-text upper flag">Brasil</div>
            </v-btn>
          </v-col>
          <v-col xl="auto">
            <v-btn
              class="barra-brasil-btn"
              block
              text
              outlined
              href="http://www.saude.gov.br/coronavirus"
            >
              <div style="color: red;" class="barra-brasil-text upper">Coronavirus (covid-19)</div>
            </v-btn>
          </v-col>
          <v-col xl="auto">
            <v-btn
              class="barra-brasil-btn"
              block
              text
              outlined
              href="http://www.simplifique.gov.br/"
            >
              <div class="barra-brasil-text">Simplifique!</div>
            </v-btn>
          </v-col>
          <v-col xl="auto">
            <v-btn
              class="barra-brasil-btn"
              block
              text
              outlined
              href="https://www.gov.br/pt-br/participacao-social/"
            >
              <div class="barra-brasil-text">Participe</div>
            </v-btn>
          </v-col>
          <v-col xl="auto">
            <v-btn
              class="barra-brasil-btn"
              block
              text
              outlined
              href="http://www.acessoainformacao.gov.br/"
            >
              <div class="barra-brasil-text">Acesso à informação</div>
            </v-btn>
          </v-col>
          <v-col xl="auto">
            <v-btn
              class="barra-brasil-btn"
              block
              text
              outlined
              href="http://www.planalto.gov.br/legislacao"
            >
              <div class="barra-brasil-text">Legislação</div>
            </v-btn>
          </v-col>
          <v-col xl="auto">
            <v-btn
              class="barra-brasil-btn"
              block
              text
              outlined
              href="https://gov.br/pt-br/canais-do-executivo-federal"
            >
              <div class="barra-brasil-text">Canais</div>
            </v-btn>
          </v-col>
          <v-col xl="auto">
            <v-btn
              class="barra-brasil-btn"
              text
              block
            >
              <div class="logo-libras"/>
            </v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <v-row no-gutters justify="center" class="header">
      <v-col cols="12" sm="10" md="7">
        <v-row no-gutters justify="center" style="overflow-x: auto">
          <v-col cols="auto">
            <v-row no-gutters>
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
            </v-row>
          </v-col>
          <v-spacer/>
          <v-col cols="auto">
            <v-row no-gutters>
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
          </v-col>
        </v-row>
        <v-row no-gutters align="start" justify="space-between">
          <v-col cols="12" sm="12" md="8">
            <v-row dense class="mb-4">
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
                  <v-col cols="12" class="pt-0 pb-1">
                    <h4 class="header-text">Ministério da Educação</h4>
                  </v-col>
                  <v-col cols="12" class="pt-0 pb-1">
                    <h1 class="header-title">Portal UFLA</h1>
                  </v-col>
                  <v-col cols="12" class="pt-0 pb-0">
                    <h3 class="header-subtitle">Universidade Federal de Lavras</h3>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-col>
          <v-spacer />
          <v-col cols="12" sm="12" md="4">
            <v-row no-gutters justify="end">
              <v-col cols="12" md="auto">
                <v-row no-gutters justify="end">
                  <v-col cols="12" tag="search">
                    <v-text-field
                      label="Busca Portal UFLA"
                      autofocus
                      single-line
                      type="text"
                      append-icon="mdi-magnify"
                      background-color="#ffffff"
                      class="pb-0 mb-0"
                      hide-details
                    />
                  </v-col>
                </v-row>
                <v-row no-gutters justify="end" class="pt-0 mt-0">
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
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <v-row no-gutters justify="center" class="about">
      <v-col cols="12" sm="10" md="7">
        <v-row no-gutters justify="end" align="start">
          <v-col cols="auto">
            <v-btn
              text
              block
              class="about-btn"
              href="https://ufla.br/sobre"
            >
              <div class="about-btn-text">Sobre a UFLA</div>
            </v-btn>
          </v-col>
          <v-col cols="auto">
            <v-btn
              text
              block
              class="about-btn"
              href="https://ufla.br/sobre/administracao/equipe-de-gestao"
            >
              <div class="about-btn-text">Equipe de Gestão</div>
            </v-btn>
          </v-col>
          <v-col cols="auto">
            <v-btn
              text
              block
              class="about-btn"
              href="https://ufla.br/servicos-da-ufla"
            >
              <div class="about-btn-text">Serviços da UFLA</div>
            </v-btn>
          </v-col>
          <v-col cols="auto">
            <v-btn
              text
              block
              class="about-btn"
              href="https://ufla.br/contato"
            >
              <div class="about-btn-text">Contato</div>
            </v-btn>
          </v-col>
          <v-col cols="auto">
            <v-btn
              text
              block
              class="about-btn"
              href="https://ufla.br/comunicacao/servicos1/atendimento-a-imprensa"
            >
              <div class="about-btn-text">Área de imprensa</div>
            </v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <v-row style="max-height: 50px !important">
      <v-col />
      <v-col cols="12" sm="10" md="7">
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
    <v-row justify="center">
      <v-col cols="12" sm="10" md="7">
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
                    <h3 class="menu-header-btn-text">
                      Portal UFLA
                    </h3>
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
                    <h4 class="menu-news-btn-title">
                      Notícias
                    </h4>
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
                    <h4 class="menu-header-btn-text">
                      Acesso à Informação
                    </h4>
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
            <v-row tag="content">
              <v-col>
                <h2 class="news-title">
                  Notícias
                </h2>
              </v-col>
            </v-row>
            <v-row>
              <v-col
                cols="6"
                v-for="(noticia, i) in noticias"
                :key="i"
              >
                <New
                  v-model="soundControl"
                  :reader="reader"
                  :item="noticia"
                  @listen="onListen"
                  @stop="stop"
                  class="new-container"
                  :id="`noticia-${i}`"
                  :ref="`noticia-${i}`"
                />
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
import New from '@/components/New'
import myNews from '@/assets/info/news'

export default {
  name: 'App',
  components: {
    New
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
    ],
    reader: false,
    noticias: [],
    soundControl: undefined,
    listener: new SpeechSynthesisUtterance(),
  }),
  watch: {
    reader: function (val) {
      if (val) {
        this.play('Leitor de notícias ativado! Você será redirecionado para o botão do leitor da primeira notícia')
        focus('noticias-0')
        this.$refs['noticias-0'].scrollIntoView();
      }
    }
  },
  created () {
    this.noticias = myNews.map(el => el)
  },
  methods: {
    onListen (msg) {
      this.play(msg)
    },
    async play (msg) {
      this.stop()
      this.listener.text = msg
      window.speechSynthesis.speak(this.listener)
    },
    stop () {
      window.speechSynthesis.cancel()
    }
  }
}
</script>

<style>
  .upper{
    text-transform: uppercase !important;
  }
  .flag{
    padding-left: 42px;
    background: url(data:image/svg+xml,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20width%3D%2226%22%20height%3D%2219%22%20viewBox%3D%220%200%201000%20700%22%3E%3Cpath%20fill%3D%22%2300923F%22%20d%3D%22M0%200h1000v700H0z%22%2F%3E%3Cpath%20fill%3D%22%23F8C300%22%20d%3D%22M500%2085L85%20350l415%20265%20415-265L500%2085z%22%2F%3E%3Ccircle%20fill%3D%22%2328166F%22%20cx%3D%22499%22%20cy%3D%22350%22%20r%3D%22174%22%2F%3E%3Cpath%20fill%3D%22%23FFF%22%20d%3D%22M395%20296c103%200%20199%2038%20272%20101%202-8%204-17%205-26-75-61-172-98-277-98-18%200-36%201-53%203-3%208-6%2016-9%2025%2020-3%2041-4%2063-4z%22%2F%3E%3C%2Fsvg%3E) 8px center no-repeat;
  }
  .barra-brasil-text{
    font-size: 11px;
    color: #606060;
    line-height: 19px;
    font-weight: 700;
    text-transform: initial;
  }
  .barra-brasil-btn{
    border-bottom: hidden;
    border-top: hidden;
    background: #ffffff !important;
    max-height: 32px;;
  }
  .logo-libras{
    background: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyOSIgaGVpZ2h0PSIyOSI+PGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoLTI2Ni4yNTAzOCwtMjMxLjY4NTk0KSI+PHBhdGggZD0ibTI5Mi40IDIzNy44Yy0wLjEgMC0wLjItMC4xLTAuMi0wLjIgMC0xLTEuOC0yLjYtNC4xLTIuNmwtMi41IDAtNC44IDMuNi00LjgtMy42LTIuNSAwYy0yLjQgMC00LjEgMS42LTQuMSAyLjYgMCAwLjEtMC4xIDAuMi0wLjIgMC4yLTAuMSAwLTAuMi0wLjEtMC4yLTAuMiAwLTEuNCAyLjEtMy4xIDQuNi0zLjFsMi40IDAgMC42LTAuNmMwLjEtMC4xIDAuMi0wLjEgMC4zIDBsMy45IDQuNiAzLjktNC42YzAuMS0wLjEgMC4yLTAuMSAwLjMgMGwwLjYgMC42IDIuNCAwYzIuNSAwIDQuNiAxLjcgNC42IDMuMSAwIDAuMS0wLjEgMC4yLTAuMiAwLjJ6bS0zIDEwLjRjLTAuMSAwLjctMC4yIDEtMC4zIDEgMCAwLjEtMC4xIDAuMS0wLjIgMC4xLTAuMSAwLTAuMS0wLjEtMC4xLTAuMiAwIDAgMC4xLTAuMyAwLjItMC45IDAuMS0wLjYtMC4yLTEuMS0wLjItMS4xIDAtMC4xIDAtMC4yIDAuMS0wLjIgMC4xIDAgMC4xIDAgMC4yIDAgMCAwIDAgMCAwIDAuMSAwIDAgMC4zIDAuNiAwLjIgMS4zem0tMSAwLjhjMCAwLjEtMC4xIDAuMS0wLjIgMC4xLTAuMSAwLTAuMS0wLjEtMC4xLTAuMiAwIDAgMC4xLTAuMyAwLjEtMC45IDAtMC42LTAuMy0xLjEtMC4zLTEuMSAwLTAuMSAwLTAuMiAwLjEtMC4yIDAuMSAwIDAuMSAwIDAuMiAwIDAgMCAwIDAgMCAwIDAgMCAwLjMgMC42IDAuMyAxLjMgMCAwLjctMC4xIDEtMC4yIDF6bS0wLjctMC40Yy0wLjMgMS4yLTAuOCAyLjItMC45IDIuNi0wLjIgMC40LTAuMyAwLjktMC4yIDIuMiAwIDEuMyAwIDIuMi0wLjEgMi41IDAgMC4yLTAuMiAwLjMtMC40IDAuMy0wLjIgMC0wLjMtMC4xLTAuNC0wLjQtMC4xLTAuNS0wLjMtMi42LTAuMy0yLjkgMC0wLjItMC4yLTAuNC0wLjMtMC40LTAuMSAwLTAuMiAwLjEtMC4zIDAuNS0wLjIgMC45LTAuNSAzLjEtMC42IDMuNi0wLjEgMC41LTAuMyAwLjYtMC40IDAuNi0wLjEgMC0wLjEgMC0wLjEgMCAwIDAgMCAwIDAgMC0wLjEgMC0wLjQgMC0wLjQtMC40IDAtMC41IDAuNC0zLjUgMC40LTMuOCAwLTAuMiAwLTAuMy0wLjEtMC4zLTAuMSAwLTAuMSAwLjEtMC4yIDAuMi0wLjMgMC40LTEuNyAyLjktMi4xIDMuNy0wLjEgMC4yLTAuMiAwLjItMC40IDAuMi0wLjEgMC0wLjIgMC0wLjMtMC4xLTAuMS0wLjEtMC4zLTAuNC0wLjItMC42IDAuMS0wLjIgMS41LTMuNCAxLjctMy44IDAuMS0wLjMgMC4xLTAuNS0wLjEtMC41LTAuMSAwLTAuMiAwLjEtMC40IDAuMi0wLjUgMC41LTIuNCAyLjUtMi43IDIuNy0wLjEgMC4xLTAuMiAwLjItMC4zIDAuMi0wLjEgMC0wLjItMC4xLTAuMy0wLjItMC4yLTAuMi0wLjItMC40LTAuMS0wLjYgMC4yLTAuMiAyLjYtMy4zIDMtNC4xIDAuNC0wLjcgMS0xLjktMC4yLTEuOS0wLjEgMC0wLjEgMC0wLjIgMC0wLjUgMC0wLjggMC4xLTEuMSAwLjEtMC41IDAtMC43LTAuMS0wLjgtMC4xLTAuMi0wLjEtMC42LTAuMy0wLjUtMC42IDAuMS0wLjIgMC43LTAuMSAxLTAuMiAwLjItMC4xIDAuMi0wLjEgMC4yLTAuMSAwIDAgMS4xLTAuMyAxLjgtMC43IDAuNy0wLjQgMi4zLTEuMSAyLjctMS4xIDAuMiAwIDAuNC0wLjEgMC42LTAuMSAwLjMgMCAwLjYgMCAwLjcgMC4xIDAuMyAwLjEgMC42IDAuOSAyIDEuNSAwIDAgMC42IDAuNiAwLjMgMS44em0tMTEuNyAyLjJjLTAuNC0xLjItMC42LTIuMy0wLjYtMi43LTAuMS0wLjQtMC4zLTAuOS0xLTEuOS0wLjctMS0xLjItMS44LTEuMy0yLjEtMC4xLTAuMiAwLjEtMC41IDAuNC0wLjUgMC4xIDAgMC4yIDAgMC4zIDAuMiAwLjQgMC40IDEuNyAyIDEuOSAyLjIgMC4xIDAuMSAwLjMgMC4yIDAuNCAwLjIgMC4yIDAgMC4yLTAuMSAwLjEtMC42LTAuMy0wLjktMS4zLTIuOS0xLjUtMy4zLTAuMy0wLjcgMC4xLTAuNyAwLjEtMC43IDAgMCAwLjEtMC4xIDAuMi0wLjEgMC4xIDAgMC4yIDAgMC4zIDAuMiAwLjIgMC40IDEuNiAzLjIgMS44IDMuNCAwLjEgMC4xIDAuMiAwLjIgMC4zIDAuMiAwLjEgMCAwLjEtMC4xIDAuMS0wLjMgMC0wLjUtMC4yLTMuMy0wLjMtNC4yIDAtMC4zIDAuMy0wLjUgMC41LTAuNSAwIDAgMCAwIDAgMCAwLjIgMCAwLjQgMC4yIDAuNSAwLjQgMC4xIDAuMiAwLjYgMy43IDAuNyA0LjIgMCAwLjIgMC4yIDAuNCAwLjMgMC40IDAuMSAwIDAuMi0wLjEgMC4zLTAuNCAwLjEtMC43IDAuNy0zLjQgMC43LTMuNyAwLTAuMyAwLjItMC40IDAuNC0wLjQgMCAwIDAuMSAwIDAuMSAwIDAuMiAwIDAuNCAwLjIgMC40IDAuNSAwIDAuMy0wLjMgMy43LTAuMiA0LjgtMC41IDAuMi0xIDAuNC0xLjMgMC40bDAgMCAwIDAtMC4yIDAuMWMwIDAtMC4xIDAtMC4yIDAtMC40IDAtMSAwLTEuMyAwLjYtMC4xIDAuMy0wLjIgMC42LTAuMSAwLjggMC4yIDAuNSAwLjggMC44IDAuOSAwLjkgMCAwIDAgMCAwIDAgMC4yIDAuMSAwLjUgMC4yIDEuMSAwLjIgMC4zIDAgMC42IDAgMS4xLTAuMS0wLjEgMC4yLTAuMiAwLjQtMC4zIDAuNmwtMC4xIDAuMWMtMC4yIDAuMy0wLjggMS4yLTEuOCAyLjUtMC4yIDAtMC4zIDAtMC41IDAtMC4zIDAtMC42IDAtMC45IDAuMSAwIDAtMC44LTAuMS0xLjMtMS4zem0wLjggMi4yYzAgMC4xLTAuMSAwLjEtMC4yIDAuMSAwIDAgMCAwLTAuMSAwIDAgMC0wLjYtMC4yLTEtMC44LTAuNC0wLjYtMC41LTAuOS0wLjUtMC45IDAtMC4xIDAtMC4yIDAuMS0wLjIgMC4xIDAgMC4yIDAgMC4yIDAuMSAwIDAgMC4xIDAuMyAwLjQgMC44IDAuNCAwLjUgMC45IDAuNyAwLjkgMC43IDAuMSAwIDAuMSAwLjEgMC4xIDAuMnptLTAuOSAwLjRjMCAwLjEtMC4xIDAuMS0wLjEgMC4xIDAgMC0wLjEgMC0wLjEgMCAwIDAtMC42LTAuMy0wLjktMC45LTAuNC0wLjYtMC40LTAuOS0wLjQtMSAwLTAuMSAwLjEtMC4yIDAuMS0wLjIgMC4xIDAgMC4yIDAuMSAwLjIgMC4xIDAgMCAwIDAuMyAwLjQgMC44IDAuMyAwLjUgMC44IDAuOCAwLjggMC44IDAuMSAwIDAuMSAwLjEgMC4xIDAuMnptMTQuOS0yMS44LTIwLjIgMGMtMi40IDAtNC40IDItNC40IDQuNGwwIDIwLjJjMCAyLjQgMiA0LjQgNC40IDQuNGwyMC4yIDBjMi40IDAgNC40LTIgNC40LTQuNGwwLTIwLjJjMC0yLjQtMi00LjQtNC40LTQuNCIgZmlsbD0iIzFjNGY5YyIvPjwvZz48L3N2Zz4K) 8px center no-repeat;
    top: 0;
    right: 0;
    width: 43px;
    height: 32px;
  }
  .barra-brasil{
    max-height: 32px;
  }
  .system-bar{
    background: #ffffff;
    max-height: 33px;
  }
  .header{
    background-color: #195128 !important;
    background-image: radial-gradient(ellipse at center, #17882c 1%, #00510f 100%) !important;
    color: #fff !important;
    margin: 0;
  }
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
  }
  .header-title{
    font-family: "open_sansextrabold",'Open Sans',Arial,Helvetica,sans-serif;
    font-size: 2.75em;
    line-height: .8em;
    font-weight: 800;
    letter-spacing: -1px;
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
  .about-btn{
    border: hidden;
    background: transparent !important;
    max-height: 32px;;
  }
  .about-btn-text{
    font-family: "open_sansregular",'Open Sans',Arial,Helvetica,sans-serif;
    color: #ffffff;
    font-size: 1.2em;
    line-height: 19px;
    text-transform: initial;
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
